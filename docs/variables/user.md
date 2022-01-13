---
id: user
---

# $(user)

This variable returns either the first argument in the command, or if that is unavailable, the username of the person who triggered the command, or a custom specified user (for example `$(user aiden)` would use `aiden` as the user).

:::caution Timers are not supported.

The variable will not return any value in a timer.

:::

## Example Output

If you made a shoutout command:

```
Shout out to $(user.display_name)! Go follow them at twitch.tv/$(user.login) - they were last seen playing $(user.game)!
```

You could use `!shoutout aiden`, which would produce this output:
```
Shout out to Aiden! Go follow them at twitch.tv/aiden - they were last seen playing Just Chatting! 
```

Or, you could hardcode a user, for example `!fossabot`, which would produce this output:

```
Shout out to $(user.display_name fossabot)! Go follow them at twitch.tv/$(user.login fossabot) - they were last seen playing $(user.game fossabot)!
```

## $(user.accountage)

Returns how long it has been since the user created their Twitch account.

```
4 years, 3 months and 2 days
```

## $(user.accountsince)

Returns the date that the user created their Twitch account.

```
Mon, 06 Apr 2015 23:09:03 UTC
```

## $(user.display_name)

Returns the uppercased version, or internationalized version of the users' username.

```
Aiden
```

## $(user.followers)

Returns the number of followers the user has.

```
5304
```

## $(user.game)

Returns the current Twitch directory the user is under.

```
Just Chatting
```

## $(user.login)

Returns the same as `$(user)`, the lowercase user username (otherwise known as "login").

```
aiden
```

## $(user.provider)

The platform that the message was sent from.

```
twitch
```

## $(user.provider_id)

The users' platform ID that the message was sent from.

```
87763385
```

## $(user.title)

Returns the current title on the users' Twitch channel.

```
Welcome to my stream!
```

## $(user.viewers)

Returns the current number of viewers the user has on their stream.

If they are live:
```
24
```

If they are offline:
```
[Error: Stream is offline.]
```

## $(user.views)

Returns the total number of channel profile views that the user has.

```
50463
```

## $(user.uptime)

Returns how long the user has been streaming for.

If they are live:
```
3 hours and 2 minutes
```

If they are offline:
```
[Error: Stream is offline.]
```
