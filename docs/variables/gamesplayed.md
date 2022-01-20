---
id: gamesplayed
---

# $(gamesplayed)

Returns a list of recorded directories that a broadcaster's latest stream was, or current stream is under.

:::info This feature is managed by a custom tracking system!

Fossabot only populates this list if it was part of your channel during at least one game change.

If Fossabot has just joined your channel recently, there will likely be no recorded games yet, even if you have already streamed in the past.

:::

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(gamesplayed)`

    ```
    Grand Theft Auto V, Just Chatting
    ```

#### Error Output

* In case a user has no recorded games yet, returns the following:

    ```
     [Error: User has no recorded games yet.]
    ```
