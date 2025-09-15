---
id: uptime
---

# !uptime

Returns the time that has passed since the current stream has gone live.

#### Parameters

This command does not take any parameters.

#### Example Output

* `!uptime`

    ```
    ChannelName has been live for 3 hours and 25 minutes
    ```

#### Error Output

* In case the stream is currently offline, returns the following:

    ```
    ChannelName is not live
    ```
