---
id: urldecode
---

# $(urldecode)

:::info This can be inconsistent with some programming languages.

The parsing for how queries are escaped/unescaped is often dependent on the programming language. Fossabot is written in Go and uses the native query encoder/decoders, so refer to [their docs](https://pkg.go.dev/net/url#QueryEscape) if you see inconsistencies.

:::

Encodes the passed argument for URL queries.

For example,

```
$(urldecode my+example+message)
```

would output:

```
my custom message
```
