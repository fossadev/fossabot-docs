---
id: count
---

# !count

Manages custom counters for the channel.

This command is only available to **Broadcasters** and **Moderators**.

#### Parameters

This command takes **two** *optional* parameters:
1. **Counter name** - The name of the counter to manage (required)
2. **Value** - The value to set or adjust (optional for viewing)

#### Example Output

* `!count deaths`

    ```
    Current value of 'deaths' counter is 42.
    ```

* `!count deaths +5`

    ```
    Updated 'deaths' count to 47
    ```

* `!count deaths -3`

    ```
    Updated 'deaths' count to 44
    ```

* `!count deaths 100`

    ```
    Updated 'deaths' count to 100
    ```

#### Error Output

* In case no counter name is provided, returns the following:

    ```
    Usage: !count <name> <(+|-)value>
    ```

* In case an invalid counter name is provided, returns the following:

    ```
    Error: Count name invalid. Must contain only alphanumeric, dashes, or underscores.
    ```

* In case an invalid count is specified, returns the following:

    ```
    Error: Invalid count specified.
    ```
