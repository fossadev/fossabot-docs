---
id: tweet
---

# $(tweet)

Returns the latest tweet as well as the time that has passed since it was tweeted from a specified Twitter account.

#### Parameters

This variable takes ***one*** *required* parameter that is a Twitter handle of who to fetch the most recent tweet of.

#### Example Output

* `$(tweet fossabot)`

    ```
    HeyGuys - https://twitter.com/Fossabot/status/1021723904577089536 | 1 hour and 43 minutes ago
    ```

#### Error Output

* In case no handle is provided, or the handle is invalid, returns the following:

    ```
    [Error: User not found.]
    ```
