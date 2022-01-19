---
id: twitchemotes
---

# $(twitchemotes)

Returns a list of all currently available subscriber emotes of a Twitch channel.

:::info

The maximum length of the output may cause not all currently available subscriber emotes to be listed at all times.

:::

#### Parameters

This variable takes ***one*** *optional* parameter that is a **Twitch username** of who to fetch a list of all currently available subscriber emotes of. Defaults to the current broadcaster's username if not provided.

#### Example Output

* `$(twitchemotes)`

    ```
    fossaCOOL fossaHack
    ```

* `$(twitchemotes aiden)`

    ```
    aiden1COOL aiden1Hack
    ```

#### Error Output

* In case a user has no currently available subscriber emotes, returns the following:

    ```
    [Error: Twitch API returned an error.]
    ```

* In case a user cannot be found, returns the following:

    ```
    [Error: User not found.]
    ```

* In case an invalid username is provided, returns the following:

    ```
    [Error: Invalid username.]
    ```
