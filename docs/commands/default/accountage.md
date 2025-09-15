---
id: accountage
---

# !accountage

Returns how long ago a user created their account.

#### Parameters

This command takes **one** *optional* parameter that is a **username** to check the account age of. Defaults to the command sender if not provided.

#### Example Output

* `!accountage`

    ```
    UserName created their account 3 years, 2 months, 15 days ago
    ```

* `!accountage username`

    ```
    UserName created their account 5 years, 8 months, 3 days ago
    ```

#### Error Output

* In case an invalid username is provided, returns the following:

    ```
    Error: Invalid username
    ```

* In case the user is not found, returns the following:

    ```
    Error: User not found
    ```
