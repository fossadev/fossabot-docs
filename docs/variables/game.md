---
id: game
---

# $(game)

Returns the current game directory a broadcaster is under.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the current directory of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(game)`

    ```
    Just Chatting
    ```

* `$(game fossabot)`

    ```
    <no game>
    ```

#### Error Output

* In case a user cannot be found, returns the following:

    ```
    [Error: User not found.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.] 
    ```
