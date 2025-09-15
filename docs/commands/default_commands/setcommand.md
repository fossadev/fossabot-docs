---
id: setcommand
---

# !setcommand

Creates a new custom command or updates an existing one.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *required* parameters:
1. **Command name** - The name of the command to create or update
2. **Response** - The response text for the command

#### Example Output

* `!setcommand hello Welcome to my stream!`

    ```
    (Command created or updated successfully - no output)
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !setcommand <command> <response>
    ```
