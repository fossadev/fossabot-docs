---
id: teamfighttactics
---

# $(teamfighttactics)

Returns the current [**Teamfight Tactics**](https://teamfighttactics.leagueoflegends.com/) league points and rank of a player.

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

* `$(teamfighttactics na sujin#goat)`

    ```
    sujin#goat is currently Gold IV 0 LP
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
