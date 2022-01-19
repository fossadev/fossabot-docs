---
id: repeat
---

# $(repeat)

Returns a specified phrase an arbitrary amount of times with spaces in-between.

#### Parameters

This variable takes **two** *required* parameters. The **first** parameter is **how often** the following phrase should be repeated, and the **second** parameter is the **actual phrase** that should be repeated.

#### Example Output

* `$(repeat 5 PogChamp Kappa)`

    ```
    PogChamp Kappa PogChamp Kappa PogChamp Kappa PogChamp Kappa PogChamp Kappa
    ```

#### Error Output

* In case an incorrect number of parameters is provided, returns the following:

    ```
    [Error: Usage: $(repeat 6 Phrase).]
    ```
