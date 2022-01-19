---
id: countup
---

# $(countup)

Returns the time that has passed since a specified date.

:::info This variables shares the same behavior with $(countdown)!

Both `$(countup)` and `$(countdown)` work the exact same way and only coexist for syntactic sugar.

If you provide a date **in the past**, they both will return the time that **has passed** since then, but if you provide a date **in the future** instead, they will both return the time that **is left** until then.

:::

#### Parameters

This variable takes **one** *required* parameter that is a **date string** to count up from.

* **Accepted Date Formats**
  * `2022-01-01`
  * `Jan 01 2022`
  * `01 Jan 2022`
  * `Jan 1st 2022`
  * `1st Jan 2022`
  * ...

* **Accepted Time Formats**
  * `14:00:00`
  * `02:00:00PM`
  * ...

###### A list of more supported date and time formats can be found [**here**](https://github.com/araddon/dateparse).

If you would like to specify a different timezone than coordinated universal time (UTC), you can do so by providing the UTC offset to that timezone (e.g. `GMT-0400` for EDT) at the end of the date string.

###### A list of all existing timezones can be found [**here**](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones#List).

#### Example Output

* `$(countup 2022-01-01 00:00:00)` *(January 1st, 2022 UTC)*

    ```
    17 days, 13 hours and 15 minutes
    ```

* `$(countup Jan 01 2022 00:00:00 GMT-0400)` *(January 1st, 2022 EDT)*

    ```
    17 days, 9 hours and 15 minutes 
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
