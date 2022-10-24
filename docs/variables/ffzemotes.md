---
id: ffzemotes
---

# $(ffzemotes)

Returns a list of all currently enabled FrankerFaceZ emotes of a Twitch channel.

:::info

The maximum length of the output may cause not all currently enabled FrankerFaceZ emotes to be listed at all times.

:::

#### Parameters

This variable takes **one** *optional* parameter that is a **Twitch username** of who to fetch a list of all currently enabled FrankerFaceZ emotes of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(ffzemotes)`

    ```
    POGGERS PepoDance OMEGALUL
    ```

* `$(ffzemotes aiden)`

    ```
    MONKERS PepePls pepePoint
    ```

#### Error Output

* In case a user has no currently enabled FrankerFaceZ emotes, returns the following:

    ```
    [Error: FrankerFaceZ API returned an error.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Twitch API returned an error.]
    ```

* In case a user cannot be found, or is otherwise unavailable, returns the following:

    ```
    [Error: User not found.]
    ```
