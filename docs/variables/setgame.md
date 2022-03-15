---
id: setgame
---

# $(setgame)

Changes the currently played game on stream.

#### Parameters

This variable takes **one** *required* parameter that is a **game** of what to set the stream directory to.

## Example Usage

* A command with the name `!gta` and a response of the following:

    ```
    $(setgame Grand Theft Auto V)
    ```

    If triggered by `!gta`, will change the stream directory to `Grand Theft Auto V` and return the following response:

    ```
    @Aiden Changed game to "Grand Theft Auto V"
    ```

#### Error Output

* In case an invalid game is provided, returns the following:

    ```
    [Error: Game does not exist on Twitch.]
    ```
