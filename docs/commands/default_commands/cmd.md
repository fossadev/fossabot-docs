---
id: cmd
---

# !cmd

Comprehensive command management system for custom commands.

This command is only available to **Broadcasters** and **Moderators**.

## !cmd add

Creates a new custom command for the channel.

#### Parameters

This command takes **two** *required* parameters:
1. **Command name** - The name of the command to create
2. **Response** - The response text for the command

#### Flags

This command supports the following optional flags:
- `--enable`: Enable the command (default: enabled)
- `--disable`: Disable the command
- `-g, --global <seconds>`: Set global cooldown in seconds (default: 5)
- `-u, --user <seconds>`: Set user cooldown in seconds (default: 15)
- `-n, --name <name>`: Set command name
- `-t, --type <type>`: Set response type: `reply`, `say`, `whisper`, or `mention` (default: say)
- `--addalias <alias>`: Add an alias for the command (can be used multiple times)
- `--removealias <alias>`: Remove an alias from the command (can be used multiple times)

#### Example Output

* `!cmd add hello Welcome to my stream!`

    ```
    Successfully added command "!hello"
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !cmd add <command> <response>
    ```

## !cmd edit

Modifies an existing custom command's response.

#### Parameters

This command takes **two** *required* parameters:
1. **Command name** - The name of the command to edit
2. **New response** - The new response text for the command

#### Flags

This command supports the following optional flags:
- `--enable` - Enable the command
- `--disable` - Disable the command
- `-g, --global <seconds>` - Set global cooldown in seconds
- `-u, --user <seconds>` - Set user cooldown in seconds
- `-n, --name <name>` - Set command name
- `-t, --type <type>` - Set response type: `reply`, `say`, `whisper`, or `mention`
- `--addalias <alias>` - Add an alias for the command (can be used multiple times)
- `--removealias <alias>` - Remove an alias from the command (can be used multiple times)

#### Example Output

* `!cmd edit hello Welcome to my amazing stream!`

    ```
    Successfully updated command "!hello"
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !cmd edit <command> <response>
    ```

* In case the command is not found, returns the following:

    ```
    [Error: Command with that name or alias does not exist.]
    ```

## !cmd delete

Deletes a custom command from the channel.

#### Parameters

This command takes **one** *required* parameter that is the **command name** to delete.

#### Example Output

* `!cmd delete hello`

    ```
    Successfully deleted command "!hello"
    ```

#### Error Output

* In case no command name is provided, returns the following:

    ```
    Usage: !cmd delete <command>
    ```

* In case the command is not found, returns the following:

    ```
    [Error: Command with that name or alias does not exist.]
    ```

## !cmd enable

Enables a disabled custom command.

#### Parameters

This command takes **one** *required* parameter that is the **command name** to enable.

#### Example Output

* `!cmd enable hello`

    ```
    Successfully enabled "!hello"
    ```

#### Error Output

* In case no command name is provided, returns the following:

    ```
    Usage: !cmd enable <command>
    ```

* In case the command is not found, returns the following:

    ```
    [Error: Command with that name or alias does not exist.]
    ```

* In case the command is already enabled, returns the following:

    ```
    [Error: Command is already enabled!]
    ```

## !cmd disable

Disables an enabled custom command.

#### Parameters

This command takes **one** *required* parameter that is the **command name** to disable.

#### Example Output

* `!cmd disable hello`

    ```
    Successfully disabled "!hello"
    ```

#### Error Output

* In case no command name is provided, returns the following:

    ```
    Usage: !cmd disable <command>
    ```

* In case the command is not found, returns the following:

    ```
    [Error: Command with that name or alias does not exist.]
    ```

* In case the command is already disabled, returns the following:

    ```
    [Error: Command is already disabled!]
    ```

## !cmd set

Creates or updates a custom command. If the command doesn't exist, it will be created. If it does exist, it will be updated.

#### Parameters

This command takes **two** *required* parameters:
1. **Command name** - The name of the command to create or update
2. **Response** - The response text for the command

#### Flags

This command supports the following optional flags:
- `--enable`: Enable the command (default: enabled)
- `--disable`: Disable the command
- `-g, --global <seconds>`: Set global cooldown in seconds (default: 5)
- `-u, --user <seconds>`: Set user cooldown in seconds (default: 15)
- `-n, --name <name>`: Set command name
- `-t, --type <type>`: Set response type: `reply`, `say`, `whisper`, or `mention` (default: say)
- `--addalias <alias>`: Add an alias for the command (can be used multiple times)
- `--removealias <alias>`: Remove an alias from the command (can be used multiple times)

#### Example Output

* `!cmd set hello Welcome to my stream!`

    ```
    Successfully added command "!hello"
    ```
    or
    ```
    Successfully updated command "!hello"
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !cmd set <command> <response>
    ```

## !cmd show

Displays the response of a custom command.

#### Parameters

This command takes **one** *required* parameter that is the **command name** to show.

#### Example Output

* `!cmd show hello`

    ```
    Response for [!hello]: Welcome to my stream!
    ```

#### Error Output

* In case no command name is provided, returns the following:

    ```
    Usage: !cmd show <command>
    ```

* In case the command is not found, returns the following:

    ```
    [Error: Command with that name or alias does not exist.]
    ```
