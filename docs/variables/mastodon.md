---
id: mastodon
---

# $(mastodon)

Returns the latest status as well as the time that has passed since it was tweeted from a specified [Mastodon](https://mastodon.social) account.

:::info Profile must be available through Mastodon.social

Fossabot is not able to query any Mastodon instance due to security concerns, your profile must be available through [mastodon.social](https://mastodon.social) to be retrievable by Fossabot.

:::

#### Parameters

This variable takes **one** *required* parameter that is a **Mastodon handle** of who to fetch the most recent status of.

#### Example Output

* `$(mastodon @fossabot)`

    ```
    👋 - https://mastodon.social/@fossabot/109838109407056375 | 4 minutes and 53 seconds ago
    ```

#### Error Output

* In case no handle is provided, returns the following:

    ```
    [Error: No account provided.]
    ```

* In case no handle is **not found, or not federated to mastodon.social**, returns the following:

    ```
    [Error: Account not found.]
    ```

* In case there are troubles communicating with [mastodon.social](https://mastodon.social), returns the following:

    ```
    [Error: Mastodon API.]
    ```

* In case the user does not have a public status, returns the following:

    ```
    [Error: User does not have a public status.]
    ```
