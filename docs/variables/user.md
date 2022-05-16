---
id: user
---

# $(user)

Returns a range of metadata around a (specified) user's channel that can be accessed via multiple different variable members for each unique piece of information.

:::info This variable behaves different when used inside of timers!

Timers are executed on an interval by Fossabot itself and therefore this variable behaves different when used inside of one.

If you want to use it with a timer, a valid Twitch username **must** be provided as the first parameter or Fossabot will return nothing in its place.

:::

## Example Usage

* A command with the name `!shoutout` and a response of the following:

    ```
    Shout out to $(user.display_name)! Go follow them at twitch.tv/$(user.login) - they were last seen playing $(user.game)!
    ```

    If triggered by `!shoutout aiden`, could return the following response:

    ```
    Shout out to Aiden! Go follow them at twitch.tv/aiden - they were last seen playing Just Chatting!
    ```

* A command with the name `!fossabot` and a response of the following:

    ```
    Shout out to $(user.display_name fossabot)! Go follow them at twitch.tv/$(user.login fossabot) - they were last seen playing $(user.game fossabot)!
    ```

    If triggered, could return the following response:

    ```
    Shout out to Fossabot! Go follow them at twitch.tv/fossabot - they were last seen playing <no game>!
    ```

## $(user)

Returns the same as `$(user.display_name)` and `$(touser)`, the uppercase version, or internationalized version of a user's username.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user)`

    ```
    Aiden
    ```

* `$(user fossabot)`

    ```
    Fossabot
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.accountage)

Returns the time that has passed since a user created their **Twitch account**.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.accountage)`

    ```
    6 years, 9 months, 10 days
    ```

* `$(user.accountage fossabot)`

    ```
    3 years, 6 months, 6 days
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.accountsince)

Returns the date when a user created their **Twitch account** in coordinated universal time (UTC).

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.accountsince)`

    ```
    Mon, 06 Apr 2015 23:09:03 UTC
    ```

* `$(user.accountsince fossabot)`

    ```
    Tue, 10 Jul 2018 20:56:46 UTC
    ```

## $(user.bio)

Returns the [Twitch bio](https://help.twitch.tv/s/article/channel-page-setup#Bio) a user has set on their channel.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.bio)`

    ```
    Welcome to my channel!
    ```

* `$(user.bio fossabot)`

    ```
    Fossabot is a Twitch chat bot that has all the features you need to create the ultimate chat experience for yourself and your audience. Built by the community, for the community.
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

* In case the users' bio is empty/not set, returns the following:
    
    ```
    <empty>
    ```

## $(user.display_name)

Returns the same as `$(user)` and `$(touser)`, the uppercase version, or internationalized version of a user's username.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.display_name)`

    ```
    Aiden
    ```

* `$(user.display_name fossabot)`

    ```
    Fossabot
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.followers)

Returns the current number of followers of a user.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.followers)`

    ```
    5305
    ```

* `$(user.followers fossabot)`

    ```
    10664
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.game)

Returns the current Twitch directory a user is under.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.game)`

    ```
    Just Chatting
    ```

* `$(user.game fossabot)`

    ```
    <no game>
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.login)

Returns the lowercase version of a user's username (otherwise known as *login*).

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.login)`

    ```
    aiden
    ```

* `$(user.login fossabot)`

    ```
    fossabot
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.provider)

Returns the platform a user sent the message from (i.e. twitch).

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.provider)`

    ```
    twitch
    ```

* `$(user.provider fossabot)`

    ```
    twitch
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.provider_id)

Returns the platform ID (e.g. the Twitch ID) of a user.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.provider_id)`

    ```
    87763385
    ```

* `$(user.provider_id fossabot)`

    ```
    237719657
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.title)

Returns the current stream title of a user's Twitch channel.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.title)`

    ```
    Welcome to my stream!
    ```

* `$(user.title fossabot)`

    ```
    Go to fossabot.com to add me to your stream!
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

## $(user.uptime)

Returns the time that has passed since a user's stream has gone live.

#### Parameters

This variable takes **one** *optional* parameter that is a Twitch username of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.uptime)`

    ```
    3 hours and 25 minutes
    ```

* `$(user.uptime fossabot)`

    ```
    12 hours and 2 minutes
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

* In case a user's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```

## $(user.viewers)

Returns the current number of viewers watching a user's stream.

#### Parameters

This variable takes **one** *optional* parameter that is a Twitch username of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.viewers)`

    ```
    36
    ```

* `$(user.viewers fossabot)`

    ```
    46
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```

* In case a user's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```

## $(user.views)

Returns the total number of views that a user has on their profile page.

#### Parameters

This variable takes **one** *optional* parameter that is a Twitch username of who to fetch the metadata of. Defaults to the sender if neither hardcoded nor provided at command execution, a user does not exist or is otherwise unavailable.

#### Example Output

* `$(user.views)`

    ```
    50463
    ```

* `$(user.views fossabot)`

    ```
    105046
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```
