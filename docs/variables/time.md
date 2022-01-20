---
id: time
---

# $(time)

Returns the current time in a specified timezone. Shares this behavior with `$(currenttime)`.

#### Parameters

This variable takes **one** *required* parameter that is a **valid [Time Zone Database](https://www.iana.org/time-zones) name**, and **one** *optional* parameter that is a **string of tokens** specifying the output format, which defaults to `hh:mm:ss A (z)` if not provided.

> ***A list of all existing timezones can be found [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones#List), and a list of all available tokens can be found [here](https://momentjs.com/docs/#/displaying/format/).***

#### Example Output

* `$(time Europe/London)`

    ```
    09:14:13 PM (GMT)
    ```

* `$(time America/Los_Angeles LLLL)`

    ```
    Tuesday, January 18, 2022 1:14 PM 
    ```

* `$(time Australia/Sydney YYYY/MM/DD hh:mm:ss)`

    ```
    2022/01/19 08:14:13 
    ```

#### Error Output

* In case no timezone is provided, returns the following:

    ```
    [Error: No timezone provided.]
    ```

* In case no valid timezone is provided, returns the following:

    ```
    [Error: Invalid timezone.]
    ```
