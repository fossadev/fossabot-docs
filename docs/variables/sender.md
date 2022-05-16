---
id: sender
---

# $(sender)

Returns a range of metadata around the sender's channel that can be accessed via multiple different variable members for each unique piece of information.

:::caution Timers are not supported!

Timers are executed on an interval by Fossabot itself and therefore this variable cannot be used inside of them.

If your timer iterates through existing commands that use this variable, or if this variable is used in a timer response, Fossabot will return `[Error: Cannot be executed inside of a timer]`.

:::

## $(sender)

Returns the same as `$(sender.display_name)`, the uppercase version, or internationalized version of the sender's username.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender)`

    ```
    Aiden
    ```

## $(sender.accountage)

Returns the time that has passed since the sender created their **Twitch account**.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.accountage)`

    ```
    3 years, 2 months and 1 day
    ```

## $(sender.accountsince)

Returns the date when the sender created their **Twitch account** in coordinated universal time (UTC).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.accountsince)`

    ```
    Mon, 06 Apr 2015 23:09:03 UTC
    ```

## $(sender.bio)

Returns the [Twitch bio](https://help.twitch.tv/s/article/channel-page-setup#Bio) of the sender.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.bio)`

    ```
    Fossabot is a Twitch chat bot that has all the features you need to create the ultimate chat experience for yourself and your audience. Built by the community, for the community.
    ```

#### Error Output

* In case the senders' bio is empty/not set, returns the following:

    ```
    <empty>
    ```

## $(sender.display_name)

Returns the same as `$(sender)`, the uppercase version, or internationalized version of the sender's username.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.display_name)`

    ```
    Aiden
    ```

## $(sender.followers)

Returns the current number of followers of the sender.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.followers)`

    ```
    5305
    ```

## $(sender.game)

Returns the current Twitch directory the sender is under.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.game)`

    ```
    Just Chatting
    ```

## $(sender.login)

Returns the same as `$(sendername)`, the lowercase version of the sender's username (otherwise known as *login*).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.login)`

    ```
    aiden
    ```

## $(sender.provider)

Returns the platform the sender sent the message from (i.e. twitch).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.provider)`

    ```
    twitch
    ```

## $(sender.provider_id)

Returns the platform ID (e.g. the Twitch ID) of the sender.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.provider_id)`

    ```
    87763385
    ```

## $(sender.title)

Returns the current stream title of the sender's Twitch channel.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.title)`

    ```
    Welcome to my stream!
    ```

## $(sender.uptime)

Returns the time that has passed since the sender's stream has gone live.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.uptime)`

    ```
    3 hours and 25 minutes
    ```

#### Error Output

* In case the sender's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```

## $(sender.viewers)

Returns the current number of viewers watching the sender's stream.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.viewers)`

    ```
    36
    ```

#### Error Output

* In case the sender's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```

## $(sender.views)

Returns the total number of views that the sender has on their profile page.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(sender.views)`

    ```
    50463
    ```
