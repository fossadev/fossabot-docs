---
id: volume
---

# !volume

Displays or sets the playback volume for media requests.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **one** *optional* parameter:

1. **Volume** - A number between 0 and 100 representing the playback volume percentage

#### Example Output

* `!volume`

    ```
    current volume: 75%
    ```

* `!volume 50`

    ```
    changed volume to 50%!
    ```

#### Error Output

* In case an invalid volume value is provided, returns the following:

    ```
    Usage: !volume <0-100>
    ```
