---
id: nuke
sidebar_position: 1
---

# Nuke

:::caution Please read the documentation carefully and ensure you understand the risks with nuke.

Furthermore please ensure you use it reponsibly, and set it up using the command template in the dashboard. Improper usage may be enforced with a permanent ban from Fossabot.
:::

```
!nuke
```

Mass ban, delete, or timeout messages based on pattern matching or regex.

The maximum scrollback length is 10 minutes. This is a dangerous command and improper usage/abuse can risk you accidentally banning your community, please ensure you read the below information properly and [Join our Discord](https://fossabot.com/discord) if you have any questions! We're always willing to help out those who need more clarity.

After each nuke, you will be whispered a nuke report of all the data that Fossabot gathered/used to nuke the chat. It will be whispered to the moderator who made the nuke. The nuke report also contains a "rollback", you can take that rollback url and execute it with `!filesay <rollback url>` if you accidentally caused more damage in your nuke (ie, banned everyone in chat).

## Parameters

This variable takes no parameters.

## Example usage

### Standard match with timeouts 

```
!nuke my bad phrase 3m 10m

"my bad phrase" - the phrase I want to remove from chat, if a user has a message which this phrase anywhere in the message, it will be removed.
3m - scroll back 3 minutes in chat to start scanning
10m - time the users out for 10 minutes
```

### Standard match with deleting messages

```
!nuke example phrase 5m delete

"example phrase" - the phrase I want to remove from chat, if a user has a message which this phrase anywhere in the message, it will be removed.
5m - scroll back 5 minutes in chat to start scanning
delete - delete the messages in chat, this is not a timeout.
```

### Match with regex and permanently ban

In order to match with regex in nuke, wrap your regular expression with `/` like so:

```
!nuke /some.+bad(regex)?here/ 2m ban

"/some.+bad(regex)?here/" - the regular expression that messages must match, ie "some.+bad(regex)?here".
2m - scroll back 2 minutes in chat to start scanning
ban - permanently ban the user from chat
```

## Radiation

Nuke also offers "radiation", which is a way to persist a nuke for up to 10 minutes, in order to use radiation, use the `-r` flag in your message to signal to Fossabot that you would like to persist your nuke (ie, remove messages from users who say the banned phrase in the future).

:::info Radiation is powered by the Blocked Terms feature in Fossabot.

To disable ongoing radiation, you should delete the blocked term in the dashboard.
:::

### Example usage

```
!nuke my bad phrase -r=5m 3m 10m

"my bad phrase" - the phrase you want to match against
"-r=5m" - radiate the nuke (ie persist) for 5 minutes
"3m" - scrollback for 3 minutes
"10m" - timeout the users who match this phrase for 10 minutes
```