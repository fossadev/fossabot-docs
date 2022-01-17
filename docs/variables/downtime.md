---
id: downtime
---

# $(downtime)

Returns the time that has passed since a user's stream has gone offline.

#### Parameters

This variable takes **one** *optional* parameter that is a Twitch username of who to fetch the downtime of. Defaults to the sender's username if not provided.

#### Example Output

* `$(downtime)`

    ```
    3 hours and 25 minutes
    ```

* `$(downtime fossabot)`

    ```
    12 hours and 2 minutes
    ```

#### Error Output

* In case a users's stream is currently live, returns the following:

    ```
    [Error: Stream is live.]
    ```

* In case a users's stream has never been live before, returns the following:

    ```
    [Error: User has no recorded downtime yet.]
    ```
