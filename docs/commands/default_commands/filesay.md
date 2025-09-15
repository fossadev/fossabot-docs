---
id: filesay
---

# !filesay

Reads and sends messages from a text file to chat.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **one** *required* parameter that is a **URL** to a text file.

#### Example Output

* `!filesay https://example.com/messages.txt`

    ```
    (No output - command executes silently)
    ```

#### Error Output

* In case no URL is provided, returns the following:

    ```
    Usage: !filesay <url>
    ```

* In case filesay is not supported on the platform, returns the following:

    ```
    Filesay is not supported on this platform.
    ```

* In case an invalid URL is provided, returns the following:

    ```
    Error: Invalid URL.
    ```


