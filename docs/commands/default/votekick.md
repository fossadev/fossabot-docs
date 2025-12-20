---
id: votekick
---

# !votekick

Starts a vote kick poll to remove a user from chat.

:::info

You can configure vote kick settings (including vote keywords, duration, and thresholds) in your votekick module settings.

:::

#### Parameters

This command takes **one** *required* parameter:

1. **Username** - The username of the user to vote kick

#### Example Output

* `!votekick username`

    ```
    Aiden has started a poll to remove UserName from chat. Vote in chat by typing VoteYea or VoteNay!
    ```

#### Error Output

* In case no username is provided, returns the following:

    ```
    Usage: !votekick <username>
    ```

* In case the user could not be found, returns the following:

    ```
    Error: Could not find user to votekick!
    ```

* In case another vote kick is already in progress, returns the following:

    ```
    Error: Another vote kick is already in progress!
    ```
