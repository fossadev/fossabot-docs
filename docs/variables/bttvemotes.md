---
id: bttvemotes
---

# $(bttvemotes)

Returns a list of all currently enabled BTTV emotes of a Twitch channel.

:::info

The maximum length of the output may cause not all currently enabled BTTV emotes to be listed at all times.

:::

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch a list of all currently enabled BTTV emotes of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(bttvemotes)`

    ```
    POGGERS PepoDance OMEGALUL
    ```

* `$(bttvemotes aiden)`

    ```
    MONKERS PepePls pepePoint
    ```

#### Error Output

* In case a user has no currently enabled BTTV emotes, returns the following:

    ```
    [Error: BetterTTV API returned an error.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Twitch API returned an error.]
    ```

* In case a user cannot be found, or is otherwise unavailable, returns the following:

    ```
    [Error: User not found.]
    ```
