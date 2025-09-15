---
id: followage
---

# !followage

Returns how long one user has been following another user.

#### Parameters

This command takes **two** *optional* parameters:
1. **Channel name**: The username of the follower (defaults to the command sender)
2. **User name**: The username of the user being followed (defaults to the broadcaster)

#### Example Output

* `!followage`

    ```
    UserName has been following ChannelName for 2 years, 3 months, 15 days
    ```

* `!followage username1 username2`

    ```
    UserName1 has been following UserName2 for 1 year, 6 months, 2 days
    ```

#### Error Output

* In case a user tries to check their own followage, returns the following:

    ```
    Error: You cannot follow yourself
    ```

* In case an invalid username is provided, returns the following:

    ```
    Error: Invalid username
    ```

* In case one or more users are not found, returns the following:

    ```
    Error: One or more users not found
    ```

* In case a user is not following the specified channel, returns the following:

    ```
    UserName is not following ChannelName
    ```
