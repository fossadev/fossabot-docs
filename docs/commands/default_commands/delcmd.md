---
id: delcmd
---

# !delcmd

Deletes a custom command from the channel.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **one** *required* parameter that is the **command name** to delete.

#### Example Output

* `!delcmd hello`

    ```
    Successfully deleted command "!hello"
    ```

#### Error Output

* In case no command name is provided, returns the following:

    ```
    Usage: !delcmd <command>
    ```
