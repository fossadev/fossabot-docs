---
id: countdown
---

# $(countdown)

Returns the time that is left until a certain date has passed. Shares this behaviour with `$(countup)`.

#### Parameters

This variable takes ***one*** *required* parameter that is a date string to count down to.

* **Accepted Date Formats**
  * `2030-01-01`
  * `Jan 01 2030`
  * `01 Jan 2030`
  * `Jan 1st 2030`
  * `1st Jan 2030`

* **Accepted Time Formats**
  * `14:00:00`
  * `02:00:00PM`

If you would like to specify a different timezone than coordinated universal time (UTC), you can do so by providing the UTC offset to that timezone (e.g. `GMT-0400` for EDT) at the end of the date string.

You can find a list of all timezones [**here**](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

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
    [Error: No timestamp provided]
    ```

* In case an invalid date string is provided, returns the following:

    ```
    [Error: Failed to parse timestamp]
    ```
