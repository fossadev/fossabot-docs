---
id: math
---

# $(math)

Returns the result of a [**math.js**](https://mathjs.org/) expression that is executed on a remote server.

#### Parameters

This variable takes ***one*** *required* parameter that is a **supported mathematical expression**.

#### Example Output

* `$(math 1 + 1)`

    ```
    2
    ```

* `$(math a = 5.08 cm + 2 inch)`

    ```
    10.16 cm
    ```

#### Error Output

* In case no expression is provided, returns the following:

    ```
    [Error: No math provided.]
    ```

* In case an invalid expression is provided, returns the following:

    ```
    [Error: Math.js API returned error 400.]
    ```
