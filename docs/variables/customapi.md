---
id: customapi
---

# $(customapi)

Allows you to get the response of a HTTP GET request to a specified URL.

There is no example output, this is solely dependent on what the API returns, Fossabot ignores all status codes, and returns the raw body contents.

## Developers

Fossabot supports a few custom HTTP headers that you may use to build deeper integrations.

## IP Ranges

Fossabot's proxy does not use a consistent IP range to send requests. You cannot rely on it for authenticating endpoints, it's recommended you include a key query parameter or something to authenticate users, we don't print customapi URLs on public commands pages.

## Common Headers

These headers are present on all customapi requests.

|              Name               |                                        Value                                        |
| :-----------------------------: | :---------------------------------------------------------------------------------: |
|     `x-fossabot-channelid`      |                        Internal channel ID of fossaobt user.                        |
| `x-fossabot-channeldisplayname` |      The uppercased version, or internationalized version of the channel name       |
|    `x-fossabot-channellogin`    |                 The lowercase channel name (also known as "login")                  |
|    `x-fossabot-channelslug`     |         The **Fossabot channel URL**. Useful for linking to commands pages.         |
|  `x-fossabot-channelprovider`   |                     The platform it was sent from, eg. `twitch`                     |
| `x-fossabot-channelproviderid`  |                       The platforms channel ID, ie: Twitch ID                       |
|     `x-fossabot-hasmessage`     | `true` or `false` depending on whether a message sent this (`false` if timer, etc). |
|          `user-agent`           |                                `Fossabot Web Proxy`                                 |

## Headers for Messages

These headers are for requests sent from messages, therefore are attached to a particular user.

|                 Name                 |                                                                    Value                                                                     |
| :----------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------: |
|       `x-fossabot-message-id`        |                                                 The message ID from the provider, eg. Twitch                                                 |
|    `x-fossabot-message-userlogin`    |                                         The lowercase username of the sender (also known as "login")                                         |
| `x-fossabot-message-userdisplayname` |                                 The uppercased version, or internationalized version of the sender username                                  |
|  `x-fossabot-message-userprovider`   | The platform the message was sent from by the user (this is useful if a discord user toggles a twitch command through the discord bot, etc). |
| `x-fossabot-message-userproviderid`  |                                                   The senders' platform ID, ie: Twitch ID                                                    |
