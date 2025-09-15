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

#### Flags

This command supports the following optional flags:

* `--enable`: Enable the command (default: enabled)
* `--disable`: Disable the command
* `-g, --global <seconds>`: Set global cooldown in seconds (default: 5)
* `-u, --user <seconds>`: Set user cooldown in seconds (default: 15)
* `-n, --name <name>`: Set command name
* `-t, --type <type>`: Set response type: `reply`, `say`, `whisper`, or `mention` (default: say)
* `--addalias <alias>`: Add an alias for the command (can be used multiple times)
* `--removealias <alias>`: Remove an alias from the command (can be used multiple times)

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
