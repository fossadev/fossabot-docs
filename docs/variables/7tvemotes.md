---
id: 7tvemotes
---

# $(7tvemotes)

Returns a list of all currently enabled 7tv emotes of a Twitch channel.

:::info

The maximum length of the output may cause not all currently enabled 7tv emotes to be listed at all times.

:::

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch a list of all currently enabled 7tv emotes of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(7tvemotes)`

    ```
    POGGERS PepoDance OMEGALUL
    ```

* `$(7tvemotes aiden)`

    ```
    MONKERS PepePls pepePoint
    ```

#### Error Output

* In case a user has no currently enabled 7tv emotes, returns the following:

    ```
    [Error: No 7tv emotes found.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Twitch API returned an error.]
    ```

* In case a user cannot be found, or is otherwise unavailable, returns the following:

    ```
    [Error: User not found.]
    ```
