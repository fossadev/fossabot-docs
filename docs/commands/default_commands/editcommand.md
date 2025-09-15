---
id: editcommand
---

# !editcommand

Modifies an existing custom command's response.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *required* parameters:
1. **Command name** - The name of the command to edit
2. **New response** - The new response text for the command

#### Example Output

* `!editcommand hello Welcome to my amazing stream!`

    ```
    (Command updated successfully - no output)
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !editcommand <command> <response>
    ```
