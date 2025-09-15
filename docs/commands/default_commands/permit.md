---
id: permit
---

# !permit

Temporarily prevents a user from being timed out.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *optional* parameters:

1. **Username** - The user to permit (required)
2. **Seconds** - Duration in seconds (defaults to 60, maximum 3600)

#### Example Output

* `!permit username`

    ```
    UserName will not get timed out for the next 60 seconds
    ```

* `!permit username 300`

    ```
    UserName will not get timed out for the next 300 seconds
    ```

#### Error Output

* In case no username is provided, returns the following:

    ```
    Usage: !permit [user] [seconds (default 60)]
    ```

* In case the user is not found, returns the following:

    ```
    Error: User not found
    ```
