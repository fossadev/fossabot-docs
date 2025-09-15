---
id: nuke
---

# !nuke

Removes messages containing a specific phrase from chat history and applies moderation actions.

This command is only available to **Broadcasters** and **Moderators**.

:::info

For detailed information about nuke functionality, usage examples, and advanced features, see the [**Nukes documentation**](/docs/nukes/usage).

:::

#### Parameters

This command takes **three** *required* parameters:
1. **Phrase** - The text or regex pattern to search for
2. **Scrollback** - How far back in chat history to search (time expression)
3. **Action** - The moderation action to take (timeout/delete/ban)

#### Example Output

* `!nuke spam 1h 300s`

    ```
    (No output - command executes silently)
    ```

* `!nuke /badword/ 30m ban`

    ```
    (No output - command executes silently)
    ```

#### Error Output

* In case insufficient parameters are provided, returns the following:

    ```
    Usage: !nuke <phrase> <scrollback> <timeout/delete/ban>
    ```

* In case nuke is not supported on the platform, returns the following:

    ```
    Nuke is not supported on this platform.
    ```
