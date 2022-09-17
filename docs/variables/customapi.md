---
id: customapi
---

# $(customapi)

Returns the response of a HTTP GET request to a specified URL.

#### Parameters

This variable takes **one** _required_ parameter that is a **URL** to send the HTTP GET request to.

#### Example Output

There is no example output as it solely depends on what the requested URL returns.

#### Error Output

- In case an invalid URL is provided, or the remote server cannot be reached, returns the following:

  ```
  [Error: Failed to connect to remote server.]
  ```

### Developers

**All status codes** will be **ignored** and only the **raw body content** of the requested URL will be returned.

Fossabot also sends multiple custom HTTP headers that you can use to build deeper integrations, a list of them can be found below.

:::tip

Use our [API endpoints](#api-endpoints) to validate whether a request originated from Fossabot, or obtain more data about the request.
:::

### IP Ranges

Fossabot's proxy **does not** use a consistent IP range to send requests. You **cannot** rely on it for authenticating endpoints!

We recommended that you use our [API Endpoints](#api-endpoints) to validate whether a given request actually came from Fossabot.

**For that reason we do NOT print customapi URLs on public commands pages.**

### List of Common Headers

These headers are present in **all** requests.

|              Name               |                                              Value                                               |
| :-----------------------------: | :----------------------------------------------------------------------------------------------: |
|     `x-fossabot-channelid`      |                          The internal **Fossabot ID** of a broadcaster.                          |
| `x-fossabot-channeldisplayname` |         The uppercase version, or internationalized version of a broadcaster's username.         |
|    `x-fossabot-channellogin`    |         The lowercase version of a broadcaster's username (otherwise known as _login_).          |
|    `x-fossabot-channelslug`     |       The **Fossabot channel URL** of a broadcaster. Useful for linking to commands pages.       |
|  `x-fossabot-channelprovider`   |                     The platform the request was sent from (e.g. `twitch`).                      |
| `x-fossabot-channelproviderid`  |                      The platform ID (e.g. the Twitch ID) of a broadcaster.                      |
|   `x-fossabot-customapitoken`   | Token that uniquely identifies this request. Use this with our [API endpoints](#api-endpoints).  |
|     `x-fossabot-hasmessage`     | `true` or `false` depending on whether a message triggered this request (`false` if timer, etc). |
|    `x-fossabot-validateurl`     |  Refer to [Validating requests](#validating-requests) for more information about this endpoint.  |
|          `user-agent`           |                                       `Fossabot Web Proxy`                                       |

### List of Message Headers

These headers are present in requests **sent from messages** and therefore attached to a particular user.

|                 Name                 |                                                                    Value                                                                     |
| :----------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------: |
|       `x-fossabot-message-id`        |                                               The message ID from the provider (e.g. Twitch).                                                |
|    `x-fossabot-message-userlogin`    |                                 The lowercase version of the sender's username (otherwise known as _login_).                                 |
| `x-fossabot-message-userdisplayname` |                                The uppercase version, or internationalized version of the sender's username.                                 |
|  `x-fossabot-message-userprovider`   | The platform the message was sent from by the user (this is useful if a Discord user toggles a Twitch command through the Discord bot, etc). |
| `x-fossabot-message-userproviderid`  |                                             The platform ID (e.g. the Twitch ID) of the sender.                                              |

### API Endpoints

Fossabot exposes two API endpoints that you may use to either validate that a given customapi request originated from Fossabot, or obtain more data that would you to customize how you respond to a given request.

:::info These endpoints are ratelimited.

Refer to [Ratelimits](#ratelimits) for more information.
:::

:::caution Tokens expire after 60 seconds.

You will receive a `token_invalid` error when sending a request to these endpoints if the token has expired.
:::

#### Validating requests

:::info This is a single use endpoint.

This means that you will only receive a valid token response the first time you call this endpoint. If you call this endpoint twice using the same token, the second request will return an error.
:::

Fossabot exposes a **single use endpoint** to let you validate whether a given customapi request actually came from Fossabot.

```
GET https://api.fossabot.com/v2/customapi/validate/<token>
```

##### Valid token

A valid token will result in HTTP status code `200` with the following body:

```
{
	"context_url": "https://api.fossabot.com/v2/customapi/context/<token>"
}
```

You may send a GET request to the value of `context_url` to obtain more data about the incoming request. Refer to [Getting context](#getting-context) for more information.

##### Invalid token

An invalid token will return HTTP status code `400` with the following body:

```
{
	"code": "token_invalid",
	"error": "Bad Request",
	"message": "Invalid token",
	"status": 400
}
```

#### Getting context

```
GET https://api.fossabot.com/v2/customapi/context/<token>
```

#### Valid token

A valid token will return HTTP status code `200` with the following body:

```
{
	"channel": {
		"id": "1",
		"login": "aiden",
		"display_name": "Aiden",
		"avatar": "https://static-cdn.jtvnw.net/jtv_user_pictures/aiden-profile_image-6d03ccc5d668cc80-300x300.jpeg",
		"slug": "aiden",
		"broadcaster_type": "affiliate",
		"provider": "twitch",
		"provider_id": "87763385",
		"created_at": "2021-07-10T04:20:05.599789Z",
		"stream_timestamp": "2022-09-17T19:17:27Z",
		"is_live": true
	},
	"message": {
		"id": "ae9a4e3e-d495-4d75-aec6-8965e7c4ccd0",
		"content": "!testcommand",
		"provider": "twitch",
		"user": {
			"provider_id": "87763385",
			"login": "aiden",
			"display_name": "Aiden",
			"roles": [
				{
					"id": "1",
					"name": "Broadcaster",
					"type": "broadcaster"
				},
				{
					"id": "3",
					"name": "Moderator",
					"type": "moderator"
				},
				{
					"id": "5",
					"name": "Subscriber",
					"type": "subscriber"
				},
				{
					"id": "269",
					"name": "test",
					"type": "custom"
				},
				{
					"id": "14",
					"name": "Admin",
					"type": "custom"
				}
			]
		}
	}
}
```

##### Invalid token

An invalid token will return HTTP status code `400` with the following body:

```
{
	"code": "token_invalid",
	"error": "Bad Request",
	"message": "Invalid token",
	"status": 400
}
```

#### Ratelimits

Fossabot uses a [leaky bucket ratelimiter](https://en.wikipedia.org/wiki/Leaky_bucket) to protect its services from abuse. You will receive a `429` HTTP status code with the following body if you exceed the rate limit:

```
{
	"code": "ratelimit",
	"error": "Too Many Requests",
	"message": "You are being rate limited.",
	"status": 429
}
```

**Rate limits may change at any time.** Use the following headers to throttle your requests accordingly:

|          Name           |                                               Value                                                |
| :---------------------: | :------------------------------------------------------------------------------------------------: |
|   `x-ratelimit-total`   |                              The total size of your ratelimit bucket                               |
| `x-ratelimit-remaining` |                               The remaining requests in your bucket                                |
|   `x-ratelimit-reset`   | A [unix timestamp](https://en.wikipedia.org/wiki/Unix_time) of when your bucket is fully refilled. |