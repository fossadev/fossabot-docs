---
id: urldecode
---

# $(urldecode)

Returns a decoded version of URL encoded input.

:::info The parsing for how queries are escaped/unescaped is often dependent on the programming language.

Fossabot is written in Go and uses the native query encoders/decoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#QueryUnescape) if you come across any inconsistencies.

:::

#### Parameters

This variable takes **one** *required* parameter that is **encoded input** that is supposed to be decoded.

#### Example Output

* `$(urldecode my+example+input)`

    ```
    my example input
    ```
