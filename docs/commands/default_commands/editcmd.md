---
id: editcmd
---

# !editcmd

Modifies an existing custom command's response.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *required* parameters:

1. **Command name** - The name of the command to edit
2. **New response** - The new response text for the command

#### Flags

This command supports the following optional flags:

* `--enable`: Enable the command
* `--disable`: Disable the command
* `-g, --global <seconds>`: Set global cooldown in seconds
* `-u, --user <seconds>`: Set user cooldown in seconds
* `-n, --name <name>`: Set command name
* `-t, --type <type>`: Set response type: `reply`, `say`, `whisper`, or `mention`
* `--addalias <alias>`: Add an alias for the command (can be used multiple times)
* `--removealias <alias>`: Remove an alias from the command (can be used multiple times)

#### Example Output

* `!editcmd hello Welcome to my amazing stream!`

    ```
    Successfully updated command "!hello"
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !editcmd <command> <response>
    ```
