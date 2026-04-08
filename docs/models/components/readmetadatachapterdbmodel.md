# ReadMetadataChapterDBModel


## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `ChapterName`                                | `string`                                     | :heavy_check_mark:                           | N/A                                          |
| `WordCount`                                  | `int64`                                      | :heavy_check_mark:                           | N/A                                          |
| `CharCount`                                  | `int64`                                      | :heavy_check_mark:                           | N/A                                          |
| `StartingCharOffset`                         | `int64`                                      | :heavy_check_mark:                           | N/A                                          |
| `HasParsedHTML`                              | `*bool`                                      | :heavy_minus_sign:                           | N/A                                          |
| `HasSummary`                                 | `*bool`                                      | :heavy_minus_sign:                           | N/A                                          |
| `DurationSeconds`                            | optionalnullable.OptionalNullable[`float64`] | :heavy_minus_sign:                           | N/A                                          |
| `FileNumber`                                 | optionalnullable.OptionalNullable[`string`]  | :heavy_minus_sign:                           | N/A                                          |