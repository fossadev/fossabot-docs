---
id: settitle
---

# $(settitle)

Changes the current stream title.

#### Parameters

This variable takes **one** *optional* parameter that is a **phrase** of what to set the stream title to.

## Example Usage

* A command with the name `!settitle` and a response of the following:

    ```
    $(settitle)
    ```

    If triggered by `!settitle Playing on NoPixel 3.0 today!`, will change the stream title to `Playing on NoPixel 3.0 today!` and return the following response:

    ```
    Changed title to "Playing on NoPixel 3.0 today!"

* A command with the name `!gta` and a response of the following:

    ```
    $(settitle Playing on NoPixel 3.0 today!)
    ```

    If triggered by `!gta`, will change the stream title to `Playing on NoPixel 3.0 today!` and return the following response:

    ```
    Changed title to "Playing on NoPixel 3.0 today!"
    ```

#### Error Output

* In case no title is provided, returns the following:

    ```
    [Error: No title provided.]
    ```
