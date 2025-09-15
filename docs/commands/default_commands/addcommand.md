---
id: addcommand
---

# !addcommand

Creates a new custom command for the channel.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *required* parameters:
1. **Command name** - The name of the command to create
2. **Response** - The response text for the command

#### Example Output

* `!addcommand hello Welcome to my stream!`

    ```
    (Command created successfully - no output)
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !addcommand <command> <response>
    ```
