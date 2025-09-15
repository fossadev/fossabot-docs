---
id: game
---

# !game

Returns the current game being played and how long it has been played.

:::info Steam Integration

When the current game is available on [**Steam**](https://store.steampowered.com/), the command will also return a direct link to the game's Steam store page.

:::

#### Parameters

This command does not take any parameters.

#### Example Output

* `!game`

    ```
    ChannelName is playing Just Chatting
    ```

* `!game` (when play time is available)

    ```
    ChannelName is playing Minecraft (Play time: 2 hours and 15 minutes) | https://steamcommunity.com/app/123456
    ```
