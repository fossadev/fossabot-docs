---
id: weather
---

# $(weather)

Returns weather data for a specified location.

#### Parameters

This variable takes **one** *required* parameter that is a location of which to fetch the weather of.

#### Example Output

* `$(weather London, UK)`

    ```
    London, United Kingdom: 🌕 18 °C (64.4 °F). Feels like 18 °C (64.4 °F). 0% cloudy. Wind is blowing from the South-East. 83% humidity. Air pressure: ~1015 hPa. Visibility: 6 miles (10 km). 
    ```

#### Error Output

* In case no location is provided, returns the following:

    ```
    [Error: No Weather location provided.]
    ```
