---
id: indexes
---

# $(index)

Returns an argument provided at a specified argument index following a command name.

#### Parameters

This variable takes **one** *optional* parameter that is a **fallback response**, that will be returned if no argument at the specified argument index is provided.

## Example Usage

* A command with the name `!verycoolname` and a response of the following:

    ```
    $(index2 this is a fallback response)
    ```

    If triggered by `!verycoolname test1 test2 test3`, would return the following response:

    ```
    test2
    ```

    And if triggered by either `!verycoolname` or `!verycoolname test1`, would return the following response:

    ```
    this is a fallback response
    ```

#### Error Output

* In case no argument at the specified argument index is provided, as well as no fallback response, returns the following:

    ```
    [Error: Index <index> is not in arguments.]
    ```
