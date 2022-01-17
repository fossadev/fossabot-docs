---
id: youtube
---

# $(youtube)

Returns the latest YouTube video of a channel or the first YouTube video in a playlist.

#### Parameters

This variable takes **one** *required* parameter that is a either a **channel name**, **channel ID** or **playlist ID**.

#### Example Output

* `$(youtube xqcow)`

    ```
    xQc Cries from Laughing at Fan-Made Memes | Reddit Recap #213 - https://youtu.be/ONPkz0cHt9E
    ```

* `$(youtube UCmDTrq0LNgPodDOFZiSbsww)`

    ```
    xQc Cries from Laughing at Fan-Made Memes | Reddit Recap #213 - https://youtu.be/ONPkz0cHt9E
    ```

* `$(youtube playlist=PLKeR9CeyAc9brDTtmz6DcCQpy5mA6m9AK)`

    ```
    xQc GTA Roleplay Server NoPixel 3.0 | Episode 1 - https://youtu.be/M6dorxRzp-0
    ```

#### Error Output

* In case an invalid or no channel name, channel ID or playlist ID is provided, returns the following:

    ```
    [Error: YouTube API returned an error.]
    ```
