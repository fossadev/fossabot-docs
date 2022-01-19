---
id: querystring
---

# $(querystring)

Returns a [**URL encoded**](urlencode.md) version of all arguments provided after the first space following a command name.

:::info The parsing for how queries are escaped is often dependent on the programming language.

Fossabot is written in Go and uses the native query encoders. Please refer to the [**Go documentation**](https://pkg.go.dev/net/url#QueryEscape) if you come across any inconsistencies.

:::

#### Parameters

This variable does not take any parameters.

## Example Usage

* A command with the name `!verycoolname` and a response of the following:

    ```
    $(querystring)
    ```

    If triggered by `!verycoolname look at this cool text`, would return the following response:

    ```
    look+at+this+cool+text
    ```
