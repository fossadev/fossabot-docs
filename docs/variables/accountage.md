---
id: accountage
---

# $(accountage)

Returns the time that has passed since a user created their **Twitch account**.

#### Parameters

This variable takes **one** *optional* parameter that is a Twitch username of who to fetch the account age of. Defaults to the sender's username if not provided.

#### Example Output

* `$(accountage)`

    ```
    Fossabot created their account 3 years, 6 months, 6 days and 13 hours ago
    ```

* `$(accountage aiden)`

    ```
    Aiden created their account 6 years, 9 months, 10 days and 11 hours ago
    ```

#### Error Output

* In case a user cannot be found, or is otherwise unavailable, returns the following:

    ```
    [Error: User not found.]
    ```
