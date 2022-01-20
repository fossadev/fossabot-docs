---
id: lastfm
---

# $(lastfm)

Returns the current playing song of a specified [**last.fm**](https://www.last.fm/) profile.

#### Parameters

This variable takes **one** *required* parameter that is a **[last.fm](https://www.last.fm/) username** of who to fetch the current playing song of, and **one** *optional* parameter that is a **custom format** in which to return the song information.

* **Supported Placeholders**
  * `{songname}` - *The song's name.*
  * `{artist}` - *The song's artist(s).*

#### Example Output

* `$(lastfm aiden)`

    ```
    Fox Stevenson - Dreamland
    ```

* `$(lastfm aiden {songname} by {artist})`

    ```
    Dreamland by Fox Stevenson
    ```

#### Error Output

* In case a user cannot be found, returns the following:

    ```
    [Error: last.fm API returned an error.]
    ```

* In case no username is provided, returns the following:

    ```
    [Error: You must provide a last.fm username.]
    ```
