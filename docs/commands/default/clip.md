---
id: clip
---

# !clip

Creates a clip of the current livestream.

:::info

This command is only available for **Twitch** channels.

:::

#### Parameters

This command does not take any parameters.

#### Example Output

* `!clip`

    ```
    🎬 Clip created! https://clips.twitch.tv/HappyFunnyAmazingCoolMoment
    ```

#### Error Output

* In case the broadcaster is not live, returns the following:

    ```
    Error: The broadcaster is not live
    ```

* In case Fossabot does not have permission to create clips, returns the following:

    ```
    Error: Fossabot does not have permission to create clips on this channel!
    ```
