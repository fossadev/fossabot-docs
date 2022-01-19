---
id: leagueoflegends
---

# $(leagueoflegends)

Returns the current [**League of Legends**](https://leagueoflegends.com) league points and rank of a summoner.

#### Parameters

This variable takes ***two*** *required* parameters. The **first** parameter is the **account region** of a summoner, and the **second** parameter is the **public name** of a summoner.

* **Accepted Account Regions**
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
  * `tr` - *(Turkey)*

#### Example Output

* `$(leagueoflegends kr SKT T1 Faker)`

    ```
    SKT T1 Faker is currently Challenger I 1102 LP
    ```

#### Error Output

* In case a summoner cannot be found, returns the following:

    ```
    [Error: Summoner not found.] 
    ```

* In case a summoner is currently unranked, returns the following:

    ```
    [Error: Summoner stats not found.] 
    ```
