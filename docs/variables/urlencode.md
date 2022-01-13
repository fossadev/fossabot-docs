---
id: urlencode
---

# $(urlencode)

:::info The parsing for how queries are escaped/unescaped is often dependent on the programming language. Fossabot is written in Go and uses the native query encoder/decoders, so refer to [their docs](https://pkg.go.dev/net/url#QueryEscape) if you see inconsistencies.

Encodes the passed argument for URL queries.

For example,

```
$(urlencode my example message)
```

would output:

```
my+custom+message
```
