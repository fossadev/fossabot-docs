---
id: botuptime
---

# $(botuptime)

Returns the uptime of the current broadcaster's Fossabot shard.

:::info

Fossabot is a distributed bot that is made up of many microservices, and runs across multiple servers/processes.

This means that the uptime of your bot may be completely different to that of another channel, and it may randomly reset or change if the system decides it needs to move you to a new server. The returned time is not indicative of any platform instability as Fossabot is built to withstand large scale, full server failures.

:::

#### Parameters

This variable does not take any parameters.

#### Example Output

* `$(botuptime)`

    ```
    3 days, 2 hours and 1 minute
    ```
