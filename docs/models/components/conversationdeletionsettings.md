# ConversationDeletionSettings


## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `DeletionTimeUnixSecs`                     | optionalnullable.OptionalNullable[`int64`] | :heavy_minus_sign:                         | N/A                                        |
| `DeletedLogsAtTimeUnixSecs`                | optionalnullable.OptionalNullable[`int64`] | :heavy_minus_sign:                         | N/A                                        |
| `DeletedAudioAtTimeUnixSecs`               | optionalnullable.OptionalNullable[`int64`] | :heavy_minus_sign:                         | N/A                                        |
| `DeletedTranscriptAtTimeUnixSecs`          | optionalnullable.OptionalNullable[`int64`] | :heavy_minus_sign:                         | N/A                                        |
| `DeleteTranscriptAndPii`                   | `*bool`                                    | :heavy_minus_sign:                         | N/A                                        |
| `DeleteAudio`                              | `*bool`                                    | :heavy_minus_sign:                         | N/A                                        |