---
id: leagueoflegends
---

# $(leagueoflegends)

Returns the current [**League of Legends**](https://leagueoflegends.com) league points and rank of a player.

:::info Riot ID transition

Riot has [**announced**](https://www.riotgames.com/en/news/summoner-name-riot-ID) their intention to migrate from Summoner Names to [**Riot IDs**](https://support-leagueoflegends.riotgames.com/hc/en-us/articles/360041788533-Riot-ID-FAQ).

In response, Fossabot is changing the syntax of `$(leagueoflegends)`. From `$(leagueoflegends <region> <summoner name>)` to `$(leagueoflegends <region> <Riot#ID>)`.

For example, `$(leagueoflegends na WallisDev)` becomes `$(leagueoflegends na Aiden#Dev)`.

The variable will continue to support both methods, but as Riot phases out the use of Summoner Names, the legacy functionality will break.
:::

#### Parameters

This variable takes **two** *required* parameters. The **first** parameter is the **account region** of a player, and the **second** parameter is the [**Riot ID**](https://support-leagueoflegends.riotgames.com/hc/en-us/articles/360041788533-Riot-ID-FAQ) of the player.

* **Supported Account Regions**
  * `br` - *(Brazil)*
  * `eune` - *(Europe Nordic & East)*
  * `euw` - *(Europe West)*
  * `jp` - *(Japan)*
  * `kr` - *(Republic of Korea)*
  * `lan` - *(Latin America North)*
  * `las` - *(Latin America South)*
  * `na` - *(North America)*
  * `oce` - *(Oceania)*
  * `pbe` - *(Public Beta Environment)*
  * `ph` - *(Philippines)*
  * `ru` - *(Russia)*
  * `sg` - *(Singapore)*
  * `th` - *(Thailand)*
  * `tw` - *(Taiwan)*
  * `tr` - *(Turkey)*
  * `vn` - *(Vietnam)*

#### Example Output

* `$(leagueoflegends kr Hide on bush#KR1)`

    ```
    Hide on bush is currently Grandmaster I 789 LP
    ```

#### Error Output

* In case a Riot ID is not found, returns the following:

    ```
    [Error: Riot ID not found.]
    ```

* In case a summoner cannot be found in the given region, returns the following:

    ```
    [Error: Summoner not found.] 
    ```

* In case a summoner is currently unranked, returns the following:

    ```
    [Error: Summoner stats not found.] 
    ```
