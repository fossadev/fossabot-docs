---
id: x
---

# $(x)

Returns the latest post as well as the time that has passed since it was posted from a specified [X](https://x.com) (formerly Twitter) account.

#### Parameters

This variable takes **one** *required* parameter that is an **X username** of who to fetch the latest post of.

#### Example Output

* `$(x fossabot)`

    ```
    A new post - https://x.com/fossabot/status/456 | 4 minutes and 53 seconds ago
    ```

#### Error Output

* In case the account cannot be found, returns the following:

    ```
    [Error: User not found.]
    ```

* In case the account does not have a post, returns the following:

    ```
    [Error: Could not find a post for this user on X.]
    ```

* In case there are troubles communicating with the X API, returns the following:

    ```
    [Error: X API error.]
    ```
