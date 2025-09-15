---
id: followdate
---

# !followdate

Returns the date when one user followed another user.

#### Parameters

This command takes **two** *optional* parameters:

1. **From user** - The username of the follower (defaults to the command sender)
2. **To user** - The username of the user being followed (defaults to the channel owner)

#### Example Output

* `!followdate`

    ```
    UserName followed ChannelName on Mon, 15 Mar 2021 14:30:22 UTC
    ```

* `!followdate username1 username2`

    ```
    UserName1 followed UserName2 on Wed, 22 Jul 2020 09:15:45 UTC
    ```

#### Error Output

* In case a user tries to check their own follow date, returns the following:

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
    UserName is not following ChannelName (or Fossabot does not have access to this broadcasters' following list)
    ```
