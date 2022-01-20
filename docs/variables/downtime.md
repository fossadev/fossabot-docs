---
id: downtime
---

# $(downtime)

Returns the time that has passed since a broadcaster's stream has gone offline.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(downtime)`

    ```
    3 hours and 25 minutes
    ```

#### Error Output

* In case a users's stream is currently live, returns the following:

    ```
    [Error: Stream is live.]
    ```

* In case a user's stream has never been live while Fossabot was in their chat, returns the following:

    ```
    [Error: User has no recorded downtime yet.]
    ```
