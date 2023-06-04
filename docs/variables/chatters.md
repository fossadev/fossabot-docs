---
id: chatters
---

# $(chatters)

Returns a range of metadata around a (specified) user's channel that can be accessed via multiple different variable members for each unique piece of information.

## Example Usage

* A command with the name `!chatters` and a response of the following:

    ```
    There are currently $(chatters) people in chat!
    ```

    If triggered, could return the following response:

    ```
    There are currently 35 people in chat!
    ```

* A command with the name `!randomchatter` and a response of the following:

    ```
    A random user in chat is $(chatters.random) 👀
    ```

    If triggered, could return the following response:

    ```
    A random user in chat is Aiden 👀
    ```

## $(chatters)

Returns the same as `$(chatters.count)`, the number of users currently connected to this chat room.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(chatters)`

    ```
    35
    ```

#### Error Output

* In case [**Fossabot**](https://fossabot.com) does not have access to the chatters list, returns the following:

    ```
    [Error: Fossabot does not have access to the chatters list. Please have the broadcaster log in at fossabot.com]
    ```

* In case there is an unexpected [**Twitch**](https://twitch.tv) API error.

    ```
    [Error: Unable to query chatters list.]
    ```

## $(chatters.count)

Returns the number of users currently connected to this chat room.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(chatters.count)`

    ```
    35
    ```

#### Error Output

* In case [**Fossabot**](https://fossabot.com) does not have access to the chatters list, returns the following:

    ```
    [Error: Fossabot does not have access to the chatters list. Please have the broadcaster log in at fossabot.com]
    ```

* In case there is an unexpected [**Twitch**](https://twitch.tv) API error.

    ```
    [Error: Unable to query chatters list.]
    ```

## $(chatters.random)

Returns the same as `$(chatters.random.display_name)`, the uppercase version, or internationalized version of a user's username of a user connected to this chat room.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(chatters.random)`

    ```
    Aiden
    ```

#### Error Output

* In case [**Fossabot**](https://fossabot.com) does not have access to the chatters list, returns the following:

    ```
    [Error: Fossabot does not have access to the chatters list. Please have the broadcaster log in at fossabot.com]
    ```

* In case there is no one connected to chat, returns the following:

    ```
    [Error: Unable to find a chatter.]
    ```

* In case there is an unexpected [**Twitch**](https://twitch.tv) API error, returns the following:

    ```
    [Error: Unable to query chatters list.]
    ```

## $(chatters.random.display_name)

Returns the uppercase version, or internationalized version of a user's username of a user connected to this chat room.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(chatters.random.display_name)`

    ```
    Aiden
    ```

#### Error Output

* In case [**Fossabot**](https://fossabot.com) does not have access to the chatters list, returns the following:

    ```
    [Error: Fossabot does not have access to the chatters list. Please have the broadcaster log in at fossabot.com]
    ```

* In case there is no one connected to chat, returns the following:

    ```
    [Error: Unable to find a chatter.]
    ```

* In case there is an unexpected [**Twitch**](https://twitch.tv) API error, returns the following:

    ```
    [Error: Unable to query chatters list.]
    ```

## $(chatters.random.login)

Returns the lowercase username of a random user connected to this chat room.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(chatters.random.login)`

    ```
    aiden
    ```

#### Error Output

* In case [**Fossabot**](https://fossabot.com) does not have access to the chatters list, returns the following:

    ```
    [Error: Fossabot does not have access to the chatters list. Please have the broadcaster log in at fossabot.com]
    ```

* In case there is no one connected to chat, returns the following:

    ```
    [Error: Unable to find a chatter.]
    ```

* In case there is an unexpected [**Twitch**](https://twitch.tv) API error, returns the following:

    ```
    [Error: Unable to query chatters list.]
    ```

## $(chatters.random.provider_id)

Returns the platform ID of a random user connected to this chat room.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(chatters.random.provider_id)`

    ```
    87763385
    ```

#### Error Output

* In case [**Fossabot**](https://fossabot.com) does not have access to the chatters list, returns the following:

    ```
    [Error: Fossabot does not have access to the chatters list. Please have the broadcaster log in at fossabot.com]
    ```

* In case there is no one connected to chat, returns the following:

    ```
    [Error: Unable to find a chatter.]
    ```

* In case there is an unexpected [**Twitch**](https://twitch.tv) API error, returns the following:

    ```
    [Error: Unable to query chatters list.]
    ```
