---
id: customapi
---

# $(customapi)

Returns the response of a HTTP GET request to a specified URL.

#### Parameters

This variable takes ***one*** *required* parameter that is a URL to send the HTTP GET request to.

#### Example Output

There is no example output as it solely depends on what the requested URL returns.

#### Error Output

* In case an invalid URL is provided, or the remote server cannot be reached, returns the following:

    ```
    [Error: Failed to connect to remote server.]
    ```

### Developers

**All status codes** will be **ignored** and only the **raw body content** of the requested URL will be returned.

Fossabot also sends multiple custom HTTP headers that you can use to build deeper integrations, a list of them can be found below.

### IP Ranges

Fossabot's proxy **does not** use a consistent IP range to send requests. You **cannot** rely on it for authenticating endpoints!

We recommended that you include a key query parameter or something else to authenticate users.

**For that reason we do NOT print customapi URLs on public commands pages.**

### List of Common Headers

These headers are present in **all** requests.

|              Name               |                                             Value                                                |
| :-----------------------------: | :----------------------------------------------------------------------------------------------: |
|     `x-fossabot-channelid`      |                          The internal **Fossabot ID** of a broadcaster.                          |
| `x-fossabot-channeldisplayname` |        The uppercase version, or internationalized version of a broadcaster's username.          |
|    `x-fossabot-channellogin`    |         The lowercase version of a broadcaster's username (otherwise known as *login*).          |
|    `x-fossabot-channelslug`     |       The **Fossabot channel URL** of a broadcaster. Useful for linking to commands pages.       |
|  `x-fossabot-channelprovider`   |                     The platform the request was sent from (e.g. `twitch`).                      |
| `x-fossabot-channelproviderid`  |                      The platform ID (e.g. the Twitch ID) of a broadcaster.                      |
|     `x-fossabot-hasmessage`     | `true` or `false` depending on whether a message triggered this request (`false` if timer, etc). |
|          `user-agent`           |                                      `Fossabot Web Proxy`                                        |

### List of Message Headers

These headers are present in requests **sent from messages** and therefore attached to a particular user.

|                 Name                 |                                                                    Value                                                                     |
| :----------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------: |
|       `x-fossabot-message-id`        |                                                 The message ID from the provider (e.g. Twitch).                                              |
|    `x-fossabot-message-userlogin`    |                                The lowercase version of the sender's username (otherwise known as *login*).                                  |
| `x-fossabot-message-userdisplayname` |                                The uppercase version, or internationalized version of the sender's username.                                 |
|  `x-fossabot-message-userprovider`   | The platform the message was sent from by the user (this is useful if a Discord user toggles a Twitch command through the Discord bot, etc). |
| `x-fossabot-message-userproviderid`  |                                               The platform ID (e.g. the Twitch ID) of the sender.                                            |
