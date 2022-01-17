---
id: uptime
---

# $(uptime)

Returns the time that has passed since a user's stream has gone live.

#### Parameters

This variable takes **one** *optional* parameter that is a Twitch username of who to fetch the uptime of. Defaults to the sender's username if not provided.

#### Example Output

* `$(uptime)`

    ```
    3 hours and 25 minutes
    ```

* `$(uptime fossabot)`

    ```
    12 hours and 2 minutes
    ```

#### Error Output

* In case a users's stream is currently offline, returns the following:

    ```
    [Error: Stream is offline.]
    ```
