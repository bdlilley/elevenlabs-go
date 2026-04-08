# AutoSyncInfo


## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `MinimumFrequencyDays`                                                  | `*int64`                                                                | :heavy_minus_sign:                                                      | Maximum number of days between automatic syncs                          |
| `AutoRemove`                                                            | `*bool`                                                                 | :heavy_minus_sign:                                                      | Whether to remove the document if the URL becomes unavailable           |
| `ConsecFailures`                                                        | `*int64`                                                                | :heavy_minus_sign:                                                      | Number of consecutive sync failures                                     |
| `NextRefreshBy`                                                         | optionalnullable.OptionalNullable[`int64`]                              | :heavy_minus_sign:                                                      | Unix timestamp for the next scheduled sync or None (in case of folders) |