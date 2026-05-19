---
id: game
---

# $(game)

Returns the current game directory a broadcaster is under, and optionally, how long Fossabot has tracked the broadcaster to be playing the game.

## $(game)

An alias to `$(game.name)`.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the current directory of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(game)`

    ```
    Just Chatting
    ```

* `$(game fossabot)`

    ```
    <no game>
    ```

#### Error Output

* In case a user cannot be found, returns the following:

    ```
    [Error: User not found.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.] 
    ```

## $(game.name)

Returns the currently playing game of a given broadcaster.

#### Parameters

This variable takes **one** *optional* parameter that is a **username** of who to fetch the current game of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(game.name)`

    ```
    Just Chatting
    ```

* `$(game.name fossabot)`

    ```
    <no game>
    ```

#### Error Output

* In case a user cannot be found, returns the following:

    ```
    [Error: User not found.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.] 
    ```

## $(game.playtime)

Returns how long the broadcaster has been playing the current game.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(game.playtime)`

    ```
    3 hours, 2 minutes and 36 seconds.
    ```

#### Error Output

* In case there is no game found in the internal metadata service, returns the following:

    ```
    [Error: No game found.]
    ```
