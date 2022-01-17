---
id: urldecode
---

# $(urldecode)

:::info This can be inconsistent with some programming languages.

The parsing for how queries are escaped/unescaped is often dependent on the programming language.

Fossabot is written in Go and uses the native query encoder/decoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#QueryEscape) if you come across any inconsistencies.

:::

Returns a decoded version of a URL encoded string.

#### Parameters

This variable takes ***one*** *required* parameter that is an encoded string that is supposed to be decoded.

#### Example Output

* `$(urldecode my+example+string)`

    ```
    my example string
    ```
