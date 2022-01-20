---
id: followage
---

# $(followage)

Returns the time that has passed since a user followed a broadcaster.

#### Parameters

This variable takes **two** *optional* parameters. The **first** parameter is a **Twitch username** of a ***user*** in question, and the **second** parameter is a **Twitch username** of a ***broadcaster*** who they are following.

#### Example Output

* `$(followage)` *(current channel: fossabot)*

    ```
    Aiden has been following Fossabot for 9 days and 2 hours
    ```

* `$(followage aiden)` *(current channel: fossabot)*

    ```
    Aiden has been following Fossabot for 9 days and 2 hours
    ```

* `$(followage aiden fossabot)`

    ```
    Aiden has been following Fossabot for 9 days and 2 hours
    ```

#### Error Output

* In case a user is not following a broadcaster, returns the following:

    ```
    [Error: <user> is not following <broadcaster>.] 
    ```

* In case one or more users cannot be found, returns the following:

    ```
    [Error: One or more users not found.] 
    ```

* In case one or more invalid usernames are provided, returns the following:

    ```
    [Error: Invalid username.] 
    ```

* In case both parameters are the same valid username, or when used with no parameters by the sender in the sender's channel, returns the following:

    ```
    [Error: You cannot follow yourself.] 
    ```
