---
id: urlencode
---

# $(urlencode)

:::info This can be inconsistent with some programming languages.

The parsing for how queries are escaped/unescaped is often dependent on the programming language.

Fossabot is written in Go and uses the native query encoder/decoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#QueryEscape) if you come across any inconsistencies.

:::

Returns a URL encoded version of a string.

#### Parameters

This variable takes ***one*** *required* parameter that is a string that is supposed to be URL encoded.

#### Example Output

* `$(urlencode my example string)`

    ```
    my+example+string 
    ```
