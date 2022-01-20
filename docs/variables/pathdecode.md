---
id: pathdecode
---

# $(pathdecode)

Returns a decoded version of path encoded input.

:::info The parsing for how paths are escaped/unescaped is often dependent on the programming language.

Fossabot is written in Go and uses the native path encoders/decoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#PathUnescape) if you come across any inconsistencies.

:::

#### Parameters

This variable takes **one** *required* parameter that is **encoded input** that is supposed to be decoded.

#### Example Output

* `$(pathdecode path%20with%3Freserved%20characters)`

    ```
    path with?reserved characters
    ```
