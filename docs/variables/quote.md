---
id: quote
---

# $(quote)

Returns a channel quote by its index.

#### Parameters

This variable takes **one** *optional* parameter that is the **index** of the quote to retrieve, or, if you would like Fossabot to select a quote at random, specify `random`.

Defaults to `random` if no parameter is provided.

#### Example Output

* `$(quote 21)`

    ```
    #21: This is the 21st quote in this channel!
    ```

* `$(quote)`

    ```
    #7: This is a randomly selected quote!
    ```

* `$(quote random)`

    ```
    #16: This is a randomly selected quote!
    ```

#### Error Output

* If no quote could be found at the index provided, returns the following:

    ```
    [Error: Quote not found.]
    ```

* In case the channel does not have any quotes added to Fossabot, returns the following:

    ```
    [Error: This channel does not have any quotes.]
    ```
