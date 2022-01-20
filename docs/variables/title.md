---
id: title
---

# $(title)

Returns the current stream title of a broadcaster's Twitch channel.

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch the current stream title of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(title)`

    ```
    Welcome to my stream!
    ```
* `$(title fossabot)`

    ```
    Go to fossabot.com to add me to your stream!
    ```

#### Error Output

* In case a user cannot be found, returns the following:

    ```
    [Error: Channel not found on Twitch API.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Twitch API returned an error.]
    ```
