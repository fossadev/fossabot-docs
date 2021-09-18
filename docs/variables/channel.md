---
id: channel
---

# $(channel)

The channel variable offers a range of metadata around the broadcasters' channel on Fossabot. It takes a range of parameters that allow you to fetch unique metadata about the broadcaster.

Passing just `$(channel)` as a variable argument in Fossabot will resolve to the user lowercase channel name (otherwise known as "login"), for example: `fossabot`.

## $(channel.accountage)

Returns when the user created their **Twitch account** NOT their Fossabot account.

```
3 years, 2 months and 1 day ago.
```

## $(channel.accountsince)

Returns the date that the user created their **Twitch account** NOT their Fossabot account.

```
Mon, 06 Apr 2015 23:09:03 UTC
```

## $(channel.display_name)

Returns the uppercased version, or internationalized version of the broadcasters' channel name.

```
Fossabot
```

## $(channel.followers)

Returns the current number of followers the broadcaster has.

```
5305
```

## $(channel.id)

Returns the channels internal Fossabot ID, **not to be confused with the Twitch ID**.

```
123
```

## $(channel.login)

Returns the same as `$(channel)`, the lowercase channel name (otherwise known as "login").

```
fossabot
```

## $(channel.provider)

The platform that the account was created from (ie `twitch`).

```
twitch
```

## $(channel.provider_id)

The platform ID (eg. their Twitch ID) of the broadcaster on Fossabot. This is **not an internal Fossabot ID**. If you queried this ID with the [Twitch API](https://dev.twitch.tv/docs/api/reference#get-users), it would return the broadcaster.

```
123456789
```

## $(channel.slug)

Returns the **Fossabot channel URL** of the broadcaster. This is useful for linking to commands pages, and dashboards on Fossabot.

:::info Fossabot slugs may not match a Twitch username.

It's important to note that just like Twitch, Fossabot has to ensure that all channel URLs on the platform remain unique, therefore we handle cases where someone may have had the same name as you on Twitch before.

For example, someone named `bob` logged into Fossabot. Later, `bob` namechanged to `bob123` and never logged into Fossabot again. If you changed your username to `bob` then tried to log into Fossabot, you would likely get a randomly generated channel slug, such as `bob_2353`.

If you believe that the channel name is available and that the user that has taken your name is inactive, feel free to [reach out to us on Discord](https://fossabot.com/discord) and we may be able to help you obtain your original channel slug.

:::

```
fossabot
```

## $(channel.subscribers)

Returns the current number of users [subscribed](https://www.twitch.tv/creatorcamp/en/get-rewarded/bits-and-subscriptions/) to their Twitch channel.

```
36
```

## $(channel.uptime)

Returns the current stream uptime.

If the channel is live:
```
3 hours and 25 minutes
```

If the channel is offline:
```
[Error: Stream is offline.]
```

## $(channel.viewers)

Returns the current number of viewers watching the stream.

If the stream is live:
```
36
```

If the stream is offline:
```
[Error: Stream is offline.]
```

## $(channel.views)

Returns the total number of views that the channel has on their profile.

```
100354
```
