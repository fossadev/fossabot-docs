---
id: sr
---

# !sr

Adds a track to the media request queue using a URL or search query.

#### Parameters

This command takes **one** *required* parameter:

1. **URL or search query** - A YouTube or SoundCloud URL, or a search query to find a track on YouTube

#### Example Output

* `!sr https://youtu.be/dQw4w9WgXcQ`

    ```
    Added "Rick Astley - Never Gonna Give You Up" to the queue at position #1 (~now)
    ```

* `!sr https://youtu.be/dQw4w9WgXcQ`

    ```
    Added "Rick Astley - Never Gonna Give You Up" to the queue at position #5 (~2m 30s)
    ```

* `!sr never gonna give you up`

    ```
    Added "Rick Astley - Never Gonna Give You Up" to the queue at position #3 (~1m 15s)
    ```

#### Error Output

* In case no parameter is provided, returns the following:

    ```
    Usage: !sr <URL or search query>
    ```

* In case media request is disabled, returns the following:

    ```
    Error: Media request is currently disabled.
    ```

* In case a search query is used but YouTube is disabled, returns the following:

    ```
    Error: Using search queries is only supported on YouTube, which has been disabled by the broadcaster.
    ```

* In case an invalid URL is provided, returns the following:

    ```
    Error: Not a valid YouTube or SoundCloud URL
    ```

* In case no valid results are found for a search query, returns the following:

    ```
    Error: No valid results found on YouTube for that search query.
    ```
