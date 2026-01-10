---
id: voteskip
---

# !voteskip

Votes to skip the currently playing track. The track will be skipped once the required number of votes is reached.

#### Parameters

This command does not take any parameters.

#### Example Output

* `!voteskip` (when more votes are needed)

    ```
    Aiden voted to skip this track. 3 votes are required to skip!
    ```

* `!voteskip` (when enough votes are reached)

    ```
    ⏭️ skipping "Rick Astley - Never Gonna Give You Up"...
    ```

#### Error Output

* In case no track is currently playing, returns the following:

    ```
    Error: Cannot voteskip when there are no tracks playing.
    ```
