---
id: count
---

# $(count)

Returns the number of times a command has been executed in a channel and optionally offers the ability to create custom counting variables.

## $(count.get)

Returns the current number that is stored in a custom counting variable.

#### Parameters

This variable takes **one** *required* parameter that is a custom counting variable name. Defaults to the behavior of `$(count)` if no parameter is provided, and returns as well as increments the command usage count by `1`.

#### Example Output

* `$(count.get my-cool-variable)`

    ```
    23
    ```

#### Error Output

* In case an invalid custom counting variable name is provided, returns the following:

    ```
    [Error: Count name invalid. Must contain only alphanumeric, dashes, or underscores.]
    ```

## $(count.update)

Returns and updates the current number that is stored in a custom counting variable by `1` or a specified amount. Shares this behaviour with `$(count.increment)`.

#### Parameters

This variable takes **one** *required* parameter that is a custom counting variable name and **one** *optional* parameter that is the amount by which to increment (positive) or decrement (negative) the previously stored count.

#### Example Output

* `$(count.update my-cool-variable)` *(previously stored count: 22)*

    ```
    23
    ```

* `$(count.update my-cool-variable 10)` *(previously stored count: 22)*

    ```
    32
    ```

* `$(count.update my-cool-variable -10)` *(previously stored count: 22)*

    ```
    12
    ```

#### Error Output

* In case an invalid or no variable name is provided, returns the following:

    ```
    [Error: Count name invalid. Must contain only alphanumeric, dashes, or underscores.]
    ```

## $(count.set)

Returns and sets the current stored number in a custom counting variable to a specified amount.

#### Parameters

This variable takes **two** *required* parameters. The **first** parameter is a custom counting variable name, and the **second** parameter is the amount that should be stored in the specified custom counting variable (minimum `0`).

#### Example Output

* `$(count.set my-cool-variable 20)`

    ```
    20
    ```

#### Error Output

* In case an invalid custom counting variable name is provided, returns the following:

    ```
    [Error: Count name invalid. Must contain only alphanumeric, dashes, or underscores.]
    ```

* In case no or only one parameter is provided, returns the following:

    ```
    [Error: Usage: $(count.set <name> <count>)]
    ```
