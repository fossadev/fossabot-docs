---
id: index
slug: /variables
---

# Variables

:::info

All supported variables are listed here in the Fossabot documentation!

:::

Variables offer inline, dynamic text replacement for Fossabot responses.

## Usage

Use the `$()` syntax within your chat responses to insert dynamic data.

For example, [**$(sender)**](sender.md) allows you to mention the name of the user triggering the action, you may choose to invoke this variable within a command such as `Hello, $(sender)!`. See the below example for more details.

## Example

A command with the following configuration:

![Example of variable usage in chat](/img/variables/variable-usage-example.jpg)

...would produce the following output in [**Twitch**](https://twitch.tv) chat.

![Example of variable output in chat](/img/variables/variable-usage-output.jpg)
