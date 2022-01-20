---
id: youtube
---

# $(youtube)

Returns the latest YouTube video of a channel or a playlist.

#### Parameters

This variable takes **one** *required* parameter that is either a **channel name**, **channel ID** or **playlist ID**.

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
    You Wont Believe This Great Escape - https://youtu.be/6nXBfJ3ZGE4 
    ```

#### Error Output

* In case an invalid or no channel name, channel ID or playlist ID is provided, returns the following:

    ```
    [Error: YouTube API returned an error.]
    ```
