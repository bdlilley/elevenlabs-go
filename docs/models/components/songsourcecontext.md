# SongSourceContext


## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `SourceType`                                        | `*string`                                           | :heavy_minus_sign:                                  | N/A                                                 |
| `SongID`                                            | `string`                                            | :heavy_check_mark:                                  | N/A                                                 |
| `Title`                                             | optionalnullable.OptionalNullable[`string`]         | :heavy_minus_sign:                                  | N/A                                                 |
| `Description`                                       | optionalnullable.OptionalNullable[`string`]         | :heavy_minus_sign:                                  | N/A                                                 |
| `Genres`                                            | []`string`                                          | :heavy_minus_sign:                                  | N/A                                                 |
| `Languages`                                         | []`string`                                          | :heavy_minus_sign:                                  | N/A                                                 |
| `IsExplicit`                                        | optionalnullable.OptionalNullable[`bool`]           | :heavy_minus_sign:                                  | N/A                                                 |
| `Bpm`                                               | optionalnullable.OptionalNullable[`int64`]          | :heavy_minus_sign:                                  | N/A                                                 |
| `GenerationSettings`                                | optionalnullable.OptionalNullable[map[string]`any`] | :heavy_minus_sign:                                  | N/A                                                 |