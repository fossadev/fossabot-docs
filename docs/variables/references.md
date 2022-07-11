---
id: references
---

# $(references)

Returns the parsed variable response from a custom command.

:::info Recursive `$(references)` invocations are blocked!

You may not call a `$(references)` variable from within another `$(references)` variable. This is to prevent service abuse.

:::

#### Parameters

This variable takes **one** *required* parameter that is the **name** of a custom command that should be referenced.

#### Example Output

Assuming an existing command of `!hello` with a response of `Hello $(user)!`, if invoked by the user `Fossabot`:

* `$(references hello)`

    ```
    Hello Fossabot!
    ```

#### Error Output

* In case a custom command does not exist:

    ```
    [Error: Command not found.]
    ```

* In case a command is not specified in the arguments:

    ```
    [Error: Input argument required.]
    ```
