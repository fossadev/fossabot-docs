---
id: pathencode
---

# $(pathencode)

Returns a path encoded version of a string.

:::info The parsing for how paths are escaped/unescaped is often dependent on the programming language.

Fossabot is written in Go and uses the native path encoders/decoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#PathEscape) if you come across any inconsistencies.

:::

#### Parameters

This variable takes **one** *required* parameter that is a string that is supposed to be encoded.

#### Example Output

* `$(pathencode path with?reserved characters)`

    ```
    path%20with%3Freserved%20characters
    ```
