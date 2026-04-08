# UsageCharactersResponseModel


## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `Time`                                                | []`int64`                                             | :heavy_check_mark:                                    | The time axis with unix timestamps for each day.      |
| `Usage`                                               | map[string][]`float64`                                | :heavy_check_mark:                                    | The usage of each breakdown type along the time axis. |