---
id: fromindex
---

# $(fromindex)

Returns all arguments provided after a specified argument index following a command name.

#### Parameters

This variable takes **one** *optional* parameter that is a **fallback response**, that will be returned if no arguments after the specified argument index are provided.

## Example Usage

* A command with the name `!verycoolname` and a response of the following:

    ```
    $(fromindex2 this is a fallback response)
    ```

    If triggered by `!verycoolname test1 test2 test3`, would return the following response:

    ```
    test2 test3
    ```

    And if triggered by only `!verycoolname`, would return the following response:

    ```
    this is a fallback response
    ```

#### Error Output

* In case no arguments after the specified argument index are provided, as well as no fallback response, returns the following:

    ```
    [Error: Index <index> is not in arguments.]
    ```
