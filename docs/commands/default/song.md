---
id: song
---

# !song

Displays the currently playing track in the media request queue.

#### Parameters

This command does not take any parameters.

#### Example Output

* `!song`

    ```
    Rick Astley - Never Gonna Give You Up, requested by Aiden https://youtu.be/dQw4w9WgXcQ
    ```

* `!song` (when track is from backup playlist)

    ```
    Rick Astley - Never Gonna Give You Up, from backup playlist https://youtu.be/dQw4w9WgXcQ
    ```

#### Error Output

* In case no song is currently playing, returns the following:

    ```
    No song is playing
    ```
