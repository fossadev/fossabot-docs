---
id: sender
---

# $(sender)

The `$(sender)` variable represents the user who sent the message.

:::caution Timers are not supported.

The variable will return `[Error: Cannot be executed inside of a timer]` if you try to use this inside of a timer.

:::

## $(sender.accountage)

Returns how long it has been since the sender created their Twitch account.

```
4 years, 3 months and 2 days
```

## $(sender.accountsince)

Returns the date that the sender created their Twitch account.

```
Mon, 06 Apr 2015 23:09:03 UTC
```

## $(sender.display_name)

Returns the uppercased version, or internationalized version of the senders' username.

```
Aiden
```

## $(sender.followers)

Returns the number of followers the sender has.

```
5304
```

## $(sender.game)

Returns the current Twitch directory the sender is under.

```
Just Chatting
```

## $(sender.login)

Returns the same as `$(sender)`, the lowercase sender username (otherwise known as "login").

```
aiden
```

## $(sender.provider)

The platform that the message was sent from.

```
twitch
```

## $(sender.provider_id)

The users' platform ID that the message was sent from.

```
87763385
```

## $(sender.title)

Returns the current title on the senders' Twitch channel.

```
Welcome to my stream!
```

## $(sender.viewers)

Returns the current number of viewers the sender has on their stream.

If they are live:
```
24
```

If they are offline:
```
[Error: Stream is offline.]
```

## $(sender.views)

Returns the total number of channel profile views that the sender has.

```
50463
```

## $(sender.uptime)

Returns how long the sender has been streaming for.

If they are live:
```
3 hours and 2 minutes
```

If they are offline:
```
[Error: Stream is offline.]
```
