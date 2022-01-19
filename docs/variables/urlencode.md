---
id: urlencode
---

# $(urlencode)

Returns a URL encoded version of a string.

:::info The parsing for how queries are escaped/unescaped is often dependent on the programming language.

Fossabot is written in Go and uses the native query encoders/decoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#QueryEscape) if you come across any inconsistencies.

:::

#### Parameters

This variable takes ***one*** *required* parameter that is a **string** that is supposed to be URL encoded.

#### Example Output

* `$(urlencode my example string)`

    ```
    my+example+string 
    ```
