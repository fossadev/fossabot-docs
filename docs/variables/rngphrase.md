---
id: rngphrase
---

# $(rngphrase)

Returns a random phrase from a specified list of phrases.

#### Parameters

This variable takes **one** *required* parameter that is a comma separated list of phrases (spaces are accepted).

#### Example Output

* `$(rngphrase Kappa,Keepo,PogChamp)`

    ```
    Keepo
    ```

#### Error Output

* If no list of phrases is provided, returns the following:

    ```
    [Error: Must provide arguments.]
    ```
