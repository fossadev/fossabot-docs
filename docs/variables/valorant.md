---
id: valorant
---

# $(valorant)

Returns a range of metadata around a broadcaster's [**Riot Games**](https://www.riotgames.com/) account, in relation to the game [**VALORANT**](https://playvalorant.com/), that can be accessed via multiple different variable members for each unique piece of information.

:::caution Authorization required!

This variable will only function if a broadcaster has authorized and connected a Riot Games account within Fossabot's dashboard under the **Integrations** tab.

:::

* **Supported Game Modes**
  * `competitive`
  * `deathmatch`
  * `escalation`
  * `premier`
  * `replication`
  * `spikerush`
  * `swiftplay`
  * `unrated`

* **Special Modifiers**
  * `include_custom` - *(adds custom games to be considered)*
  * `custom_only` - *(limits the considered games to **custom games only**)*

## $(valorant.display_name)

Returns the current name and tag of the linked [**Riot Games**](https://riotgames.com) account.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(valorant.display_name)`

    ```
    Aiden#Dev
    ```

#### Error Output

* In case we are unable to retrieve a response from [**Riot**](https://riotgames.com)'s API:

    ```
    [Error: Riot API returned an error.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.leaderboard_placement)

:::caution Data may be outdated

Due to limitations imposed by the [**Riot Games API**](https://developer.riotgames.com/docs/valorant), Fossabot's data may be stale for up to 30 minutes.

:::

Returns the current position of the broadcaster on their [**Ranked Leaderboard**](https://playvalorant.com/leaderboards).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(valorant.leaderboard_placement)`

    ```
    122
    ```

#### Error Output

* In case the Riot account does not appear in any [**Ranked Leaderboards**](https://playvalorant.com/leaderboards):

    ```
    [Error: Could not find player on any VALORANT leaderboards.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.leaderboard_wins)

:::caution Data may be outdated

Due to limitations imposed by the [**Riot Games API**](https://developer.riotgames.com/docs/valorant), Fossabot's data may be stale for up to 30 minutes.

:::

Returns the number of wins associated with the broadcaster on their [**Ranked Leaderboard**](https://playvalorant.com/leaderboards).

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(valorant.leaderboard_wins)`

    ```
    101
    ```

#### Error Output

* In case the Riot account does not appear in any [**Ranked Leaderboards**](https://playvalorant.com/leaderboards):

    ```
    [Error: Could not find player on any VALORANT leaderboards.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.rank)

Returns the current competitive rank of the broadcaster.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(valorant.rank)`

    ```
    Platinum 1
    ```

#### Error Output

* In case we are unable to retrieve a response from [**Riot**](https://riotgames.com)'s API:

    ```
    [Error: Riot API returned an error.]
    ```

* In case we are unable to resolve the Riot's internal competitive type to a label:

    ```
    <unknown>
    ```

* In case the Riot account does not have any competitive match history:

    ```
    [Error: Cannot determine rank - account does not appear to have any competitive match history.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.rank_rating)

:::caution Data may be outdated

Due to limitations imposed by the [**Riot Games API**](https://developer.riotgames.com/docs/valorant), Fossabot's data may be stale for up to 30 minutes.

:::

Returns the current [**Rank Rating (RR)**](https://support-valorant.riotgames.com/hc/articles/20113235347347) of the broadcaster.

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(valorant.rank_rating)`

    ```
    764
    ```

#### Error Output

* In case the Riot account does not appear in any [**Ranked Leaderboards**](https://playvalorant.com/leaderboards):

    ```
    [Error: Could not find player on any VALORANT leaderboards.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.stream_wins)

Returns the number of games that ended in a win for a specified game mode(s) during the current stream session.

#### Parameters

This variable takes **one** or more *optional* parameters that is a list of **game modes** which to return the current stream's amount of wins for. Defaults to all existing game modes, excluding custom games, if not provided.

#### Example Output

* `$(valorant.stream_wins)` *(all games modes, **without** custom games)*

    ```
    1
    ```

* `$(valorant.stream_wins include_custom)` *(all games modes, **with** custom games)*

    ```
    3
    ```

* `$(valorant.stream_wins custom_only)` *(all games modes, **but only** custom games)*

    ```
    2
    ```

* `$(valorant.stream_wins spikerush)` *(only Spike Rush games, **without** custom games)*

    ```
    0
    ```

#### Error Output

* In case an invalid game mode is specified, returns the following:

    ```
    [Error: Queue must be one of: competitive, deathmatch, escalation, premier, replication, spikerush, swiftplay, unrated.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.stream_losses)

Returns the number of games that ended in a loss for a specified game mode(s) during the current stream session.

#### Parameters

This variable takes **one** or more *optional* parameters that is a list of **game modes** which to return the current stream's amount of losses for. Defaults to all existing game modes, excluding custom games, if not provided.

#### Example Output

* `$(valorant.stream_losses)` *(all games modes, **without** custom games)*

    ```
    1
    ```

* `$(valorant.stream_losses include_custom)` *(all games modes, **with** custom games)*

    ```
    3
    ```

* `$(valorant.stream_losses custom_only)` *(all games modes, **but only** custom games)*

    ```
    2
    ```

* `$(valorant.stream_losses spikerush)` *(only Spike Rush games, **without** custom games)*

    ```
    0
    ```

#### Error Output

* In case an invalid game mode is specified, returns the following:

    ```
    [Error: Queue must be one of: competitive, deathmatch, escalation, premier, replication, spikerush, swiftplay, unrated.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```

## $(valorant.stream_ties)

Returns the number of games that ended in a tie for a specified game mode(s) during the current stream session.

#### Parameters

This variable takes **one** or more *optional* parameters that is a list of **game modes** which to return the current stream's amount of ties for. Defaults to all existing game modes, excluding custom games, if not provided.

#### Example Output

* `$(valorant.stream_ties)` *(all games modes, **without** custom games)*

    ```
    1
    ```

* `$(valorant.stream_ties include_custom)` *(all games modes, **with** custom games)*

    ```
    3
    ```

* `$(valorant.stream_ties custom_only)` *(all games modes, **but only** custom games)*

    ```
    2
    ```

* `$(valorant.stream_ties spikerush)` *(only Spike Rush games, **without** custom games)*

    ```
    0
    ```

#### Error Output

* In case an invalid game mode is specified, returns the following:

    ```
    [Error: Queue must be one of: competitive, deathmatch, escalation, premier, replication, spikerush, swiftplay, unrated.]
    ```

* In case the broadcaster has not yet authorized the [**Riot Games**](https://riotgames.com) integration:

    ```
    [Error: The broadcaster must first link their Riot Games account in fossabot.com -> integrations.]
    ```
