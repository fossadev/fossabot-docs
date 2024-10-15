---
id: twitchreward
---

# $(twitchreward)

:::note

Due to limitations imposed by the [**Twitch API**](https://dev.twitch.tv/docs/api/reference/#get-custom-reward-redemption), Fossabot is only able to return metadata for rewards created through the [**Fossabot dashboard**](https://fossabot.com/login). Create them through Fossabot's `Channel Points` page.

:::

Returns a range metadata around a given [**Twitch Channel Point Reward**](https://help.twitch.tv/s/article/channel-points-guide).

## $(twitchreward)

:::info

Fossabot only counts up to 250 unfulfilled redemptions. Rewards with more than 250 unfulfilled redemptions will return `250+`.

:::

Returns the same as `$(twitchreward.queue_depth)`, the number of unfulfilled redemptions for the reward.

#### Parameters

This variable takes *one* **required** parameter that is the **name of the [Twitch Channel Point Reward](https://help.twitch.tv/s/article/channel-points-guide)** to fetch the metadata of.

#### Example Output

* `$(twitchreward Play a game of VALORANT with me!)`

    ```
    5
    ```

* `$(twitchreward 251 people have redeemed this reward...)`

    ```
    250+
    ```

#### Error Output

* In case the reward was not found:

    ```
    [Error: Unable to find a reward with that name.]
    ```

* In case the reward was **not** created through the [**Fossabot dashboard**](https://fossabot.com/login):

    ```
    [Error: Unable to access reward, make sure you create it through fossabot.com]
    ```

## $(twitchreward.queue_depth)

:::info

Fossabot only counts up to 250 unfulfilled redemptions. Rewards with more than 250 unfulfilled redemptions will return `250+`.

:::

Returns the number of unfulfilled redemptions for the reward.

#### Parameters

This variable takes *one* **required** parameter that is the **name of the [Twitch Channel Point Reward](https://help.twitch.tv/s/article/channel-points-guide)** to fetch the metadata of.

#### Example Output

* `$(twitchreward.queue_depth Play a game of VALORANT with me!)`

    ```
    5
    ```

* `$(twitchreward.queue_depth 251 people have redeemed this reward...)`

    ```
    250+
    ```

#### Error Output

* In case the reward was not found:

    ```
    [Error: Unable to find a reward with that name.]
    ```

* In case the reward was **not** created through the [**Fossabot dashboard**](https://fossabot.com/login):

    ```
    [Error: Unable to access reward, make sure you create it through fossabot.com]
    ```

## $(twitchreward.redeemer_position)

Returns the position for the message sender in the redemption queue.

#### Parameters

This variable takes *one* **required** parameter that is the **name of the [Twitch Channel Point Reward](https://help.twitch.tv/s/article/channel-points-guide)** to fetch the metadata of.

#### Example Output

* `$(twitchreward.redeemer_position Play a game of VALORANT with me!)`

    ```
    2
    ```

#### Error Output

* In case the reward was not found:

    ```
    [Error: Unable to find a reward with that name.]
    ```

* In case the reward was **not** created through the [**Fossabot dashboard**](https://fossabot.com/login):

    ```
    [Error: Unable to access reward, make sure you create it through fossabot.com]
    ```

* In case the user does **not** have a pending redemption in the rewards queue:

    ```
    [Error: User is not in queue!]
    ```


## $(twitchreward.redeemer_position.USERNAME_OR_ID)

Returns the position for a specific user in the redemption queue. Replace `USERNAME_OR_ID` with another variable, such as [**$(user)**](/variables/user), or a hardcoded value. You may specifiy **either** a user ID, or username.

#### Parameters

This variable takes *one* **required** parameter that is the **name of the [Twitch Channel Point Reward](https://help.twitch.tv/s/article/channel-points-guide)** to fetch the metadata of.

#### Example Output

* `$(twitchreward.redeemer_position.aiden Play a game of VALORANT with me!)`

    ```
    2
    ```

* `$(twitchreward.redeemer_position.87763385 Play a game of VALORANT with me!)`

    ```
    2
    ```

#### Error Output

* In case the reward was not found:

    ```
    [Error: Unable to find a reward with that name.]
    ```

* In case the reward was **not** created through the [**Fossabot dashboard**](https://fossabot.com/login):

    ```
    [Error: Unable to access reward, make sure you create it through fossabot.com]
    ```

* In case the user does **not** have a pending redemption in the rewards queue:

    ```
    [Error: User is not in queue!]
    ```

## $(twitchreward.redeemers)

Returns the 5 oldest redeemers in the queue, sorted by oldest redemption first.

#### Parameters

This variable takes *one* **required** parameter that is the **name of the [Twitch Channel Point Reward](https://help.twitch.tv/s/article/channel-points-guide)** to fetch the metadata of.

#### Example Output

* `$(twitchreward.redeemers Play a game of VALORANT with me!)`

    ```
    Aiden, Fossabot, Rydannn, Twitch and cent.
    ```

#### Error Output

* In case the reward was not found:

    ```
    [Error: Unable to find a reward with that name.]
    ```

* In case the reward was **not** created through the [**Fossabot dashboard**](https://fossabot.com/login):

    ```
    [Error: Unable to access reward, make sure you create it through fossabot.com]
    ```

## $(twitchreward.redeemers.COUNT)

Allows you to return a custom number of redeemers in the queue, sorted by oldest redemption first. You may specify a count between `1` and `25`. A value outside of these bounds will return `5`.

#### Parameters

This variable takes *one* **required** parameter that is the **name of the [Twitch Channel Point Reward](https://help.twitch.tv/s/article/channel-points-guide)** to fetch the metadata of.

#### Example Output

* `$(twitchreward.redeemers.3 Play a game of VALORANT with me!)`

    ```
    Aiden, Fossabot and Rydannn
    ```

* `$(twitchreward.redeemers.4 Play a game of VALORANT with me!)`

    ```
    Aiden, Fossabot, Rydannn and Twitch
    ```

* `$(twitchreward.redeemers.4 Play a game of VALORANT with me!)`

    ```
    Aiden
    ```

#### Error Output

* In case the reward was not found:

    ```
    [Error: Unable to find a reward with that name.]
    ```

* In case the reward was **not** created through the [**Fossabot dashboard**](https://fossabot.com/login):

    ```
    [Error: Unable to access reward, make sure you create it through fossabot.com]
    ```
