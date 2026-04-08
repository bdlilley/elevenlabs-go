# SrtExportOptions


## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `MaxCharactersPerLine`                       | optionalnullable.OptionalNullable[`int64`]   | :heavy_minus_sign:                           | N/A                                          |
| `IncludeSpeakers`                            | `*bool`                                      | :heavy_minus_sign:                           | N/A                                          |
| `IncludeTimestamps`                          | `*bool`                                      | :heavy_minus_sign:                           | N/A                                          |
| `Format`                                     | `string`                                     | :heavy_check_mark:                           | N/A                                          |
| `SegmentOnSilenceLongerThanS`                | optionalnullable.OptionalNullable[`float64`] | :heavy_minus_sign:                           | N/A                                          |
| `MaxSegmentDurationS`                        | optionalnullable.OptionalNullable[`float64`] | :heavy_minus_sign:                           | N/A                                          |
| `MaxSegmentChars`                            | optionalnullable.OptionalNullable[`int64`]   | :heavy_minus_sign:                           | N/A                                          |