---
id: accountdate
---

# !accountdate

Returns the date when a user created their account.

#### Parameters

This command takes **one** *optional* parameter that is a **username** to check the account creation date of. Defaults to the command sender if not provided.

#### Example Output

* `!accountdate`

    ```
    UserName created their account on Mon, 06 Apr 2015 23:09:03 UTC
    ```

* `!accountdate username`

    ```
    UserName created their account on Tue, 10 Jul 2018 20:56:46 UTC
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    Error: Invalid username
    ```

* In case the user is not found, returns the following:

    ```
    Error: User not found.
    ```
