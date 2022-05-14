---
id: flags
title: Flags
slug: /keywords/flags
---

# Flags

Flags are chainable properties that are applied at the beginning of a phrase. They allow you to customize how Fossabot should parse, and match a given phrase.

For example, given the phrase `foobar`, in order to make this phrase use regex, it would become `regex:foobar`. If the phrase should also be case-sensitive, and use regex, then the phrase should be `regex:sensitive:foobar`. The order in which you chain flags is irrelevant to how Fossabot parses the phrase, as long as they all exist **before** the phrase content.

## regex:

:::info Your regex must be compatible with the [RE2](https://github.com/google/re2) regex engine!

Fossabot executes regular expressions using [RE2](https://github.com/google/re2/wiki/WhyRE2), a regex engine created by Google. Not all features are supported by this engine, and you are responsible for ensuring that your regex is compatible with this engine, else Fossabot will silently ignore it.

You can validate your regular expression by using sites such as [regex101.com](https://regex101.com/). **Make sure you select `Golang` as the regex flavor on the left sidebar.**

:::

The use of `regex:` in a phrase tells Fossabot to treat the following phrase as a [Regular Expression](https://www.regular-expressions.info/), and will test the given keyword target against the phrase.

## sensitive:

Instructs Fossabot to match your phrase with [case sensitivity](https://en.wikipedia.org/wiki/Case_sensitivity). By default, all phrases in keywords are **case insensitive**.

## negative:

Instructs Fossabot to count this phrase as a match if the phrase is **not** able to be matched against the keyword target. This is particularly useful if you create a regular expression, then want to ensure that it doesn't match particular edge cases.

For example, if you had a phrase group with the phrase `test`, and a message with `foobar` was sent, this **would count as a match** - because `test` is **not** present in `foobar`.
