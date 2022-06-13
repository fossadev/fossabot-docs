---
id: channel
---

# $(channel)

Returns a range of metadata around a broadcaster's channel that can be accessed via multiple different variable members for each unique piece of information.

## $(channel)

Returns the same as `$(channel.login)`, the lowercase version of a broadcaster's username (otherwise known as *login*).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel)`

    ```
    fossabot
    ```

## $(channel.accountage)

Returns the time that has passed since a broadcaster created their **Twitch account**.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.accountage)`

    ```
    3 years, 2 months and 1 day
    ```

## $(channel.accountsince)

Returns the date when a broadcaster created their **Twitch account** in coordinated universal time (UTC).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.accountsince)`

    ```
    Mon, 06 Apr 2015 23:09:03 UTC
    ```

## $(channel.bio)

Returns the [Twitch bio](https://help.twitch.tv/s/article/channel-page-setup#Bio) of the channel.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.bio)`

    ```
    Fossabot is a Twitch chat bot that has all the features you need to create the ultimate chat experience for yourself and your audience. Built by the community, for the community.
    ```

#### Error Output

* In case the channels' bio is empty/not set, returns the following:

    ```
    <empty>
    ```

## $(channel.display_name)

Returns the uppercase version, or internationalized version of a broadcaster's username.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.display_name)`

    ```
    Fossabot
    ```

## $(channel.followers)

Returns the current number of followers of a broadcaster.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.followers)`

    ```
    5305
    ```

## $(channel.id)

Returns the internal **Fossabot ID** of a broadcaster, **not to be confused with the Twitch ID**.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.id)`

    ```
    123
    ```

## $(channel.login)

Returns the same as `$(channel)`, the lowercase version of a broadcaster's username (otherwise known as *login*).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.login)`

    ```
    fossabot
    ```

## $(channel.provider)

Returns the platform a broadcaster's account was created on (i.e. twitch).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.provider)`

    ```
    twitch
    ```

## $(channel.provider_id)

Returns the platform ID (e.g. the Twitch ID) of a broadcaster, **not to be confused with the internal Fossabot ID**.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.provider_id)`

    ```
    237719657
    ```

## $(channel.slug)

Returns the **Fossabot channel URL** of a broadcaster. This is useful for linking to commands pages, and dashboards on Fossabot.

:::info Fossabot slugs might not match a broadcaster's username!

It's important to note that just like Twitch, Fossabot has to ensure that all channel URLs on the platform remain unique. Therefore we handle cases where someone may have had the same name as you on Twitch before in a special way.

For example, someone named **`bob`** logged into Fossabot. Later, **`bob`** namechanged to **`bob123`** and never logged into Fossabot again. If you changed your username to **`bob`** and tried to log into Fossabot, you would likely get a randomly generated channel slug such as **`bob_2353`**.

If you believe that your channel name is available and that the user that has taken your name is inactive, feel free to [**reach out to us on Discord**](https://fossabot.com/discord) and we might be able to help you obtain your original channel slug.

:::

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.slug)`

    ```
    fossabot
    ```

## $(channel.subscribers)

Returns the current number of users [**subscribed**](https://www.twitch.tv/creatorcamp/en/get-rewarded/bits-and-subscriptions/) to a broadcaster.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.subscribers)`

    ```
    36
    ```

## $(channel.subpoints)

Returns the current number of [**sub points**](https://help.twitch.tv/s/article/emote-slots?language=en_US#sub) of a broadcaster.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.subpoints)`

    ```
    46
    ```

## $(channel.uptime)

Returns the time that has passed since a broadcaster's stream has gone live.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.uptime)`

    ```
    3 hours and 25 minutes
    ```

#### Error Output

* In case a broadcaster's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```

## $(channel.viewers)

Returns the current number of viewers watching a broadcaster's stream.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.viewers)`

    ```
    36
    ```

#### Error Output

* In case a broadcaster's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```

## $(channel.views)

Returns the total number of views that a broadcaster has on their profile page.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(channel.views)`

    ```
    100354
    ```
