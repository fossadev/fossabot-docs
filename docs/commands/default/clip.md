---
id: clip
---

# !clip

Creates a clip of the current stream on Twitch.

This command is only available on **Twitch** streams.

#### Parameters

This command takes **one** *optional* parameter:

1. **Title** - The title to set for the created clip (optional)

#### Example Output

* `!clip`

    ```
    🎬 Clip created! https://clips.twitch.tv/HappyFunnyAmazingCoolMoment 
    ```

* `!clip Amazing play by the streamer!`

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
