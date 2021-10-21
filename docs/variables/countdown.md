---
id: countdown
---

# $(countdown)

Countdown tells you the amount of time until a certain date has passed.

For example, `$(countdown 2022-01-01 00:00:00)` will make the bot calculate the time until 1st Jan 2022.

```
2 months, 10 days and 2 hours
```

To use a specific timezone you can add the UTC offset to the timestamp.

For example, `$(countdown Jan 01 2022 00:00:00 GMT-0400)` would use EDT as the timezone.

```
2 months, 10 days and 6 hours
```

You can find a list of all timezones [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

**Accepted date formatting:**

- `2022-01-01`
- `Jan 01 2022`
- `01 Jan 2022`
- `Jan 1st 2022`
- `1st Jan 2022`

**Accepted time formatting:**

- `14:00:00`
- `02:00:00PM`
