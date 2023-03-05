---
id: countdown
---

# $(countdown)

Returns the time that is left until a specified date.

:::info This variables shares the same behavior with $(countup)!

Both `$(countdown)` and `$(countup)` work the exact same way and only coexist for syntactic sugar.

If you provide a date **in the future**, they will both return the time that **is left** until then, but if you provide a date **in the past** instead, they both will return the time that **has passed** since then.

:::

#### Parameters

This variable takes **one** *required* parameter that is a **date string** to count down to.

* **Supported Date Formats**
  * `2030-01-01`
  * `Jan 01 2030`
  * `01 Jan 2030`
  * `Jan 1st 2030`
  * `1st Jan 2030`
  * ...

* **Supported Time Formats**
  * `14:00:00`
  * `02:00:00PM`
  * ...

> ***A list of more supported date and time formats can be found [here](https://github.com/araddon/dateparse).***

If you would like to specify a different timezone than coordinated universal time (UTC), you can do so by providing the UTC offset to that timezone (e.g. `GMT-0400` for EDT) at the end of the date string.

> ***A list of all existing timezones can be found [here](https://wikipedia.org/wiki/List_of_tz_database_time_zones#List).***

#### Example Output

* `$(countdown 2030-01-01 00:00:00)` *(January 1st, 2030 UTC)*

    ```
    7 years, 11 months, 14 days and 9 hours
    ```

* `$(countdown Jan 01 2030 00:00:00 GMT-0400)` *(January 1st, 2030 EDT)*

    ```
    7 years, 11 months, 14 days and 13 hours
    ```

#### Error Output

* In case no date string is provided, returns the following:

    ```
    [Error: No timestamp provided.]
    ```

* In case an invalid date string is provided, returns the following:

    ```
    [Error: Failed to parse timestamp.]
    ```
