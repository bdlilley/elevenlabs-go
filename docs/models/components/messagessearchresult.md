# MessagesSearchResult

transcript_index: index of the message in the conversation transcript
chunk_text: text of the transcript; transcript messages if very long could have several chunks.
score: similarity score of the message to the search query


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `ConversationID`                            | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `AgentID`                                   | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `AgentName`                                 | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |
| `TranscriptIndex`                           | `int64`                                     | :heavy_check_mark:                          | N/A                                         |
| `ChunkText`                                 | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `Score`                                     | `float64`                                   | :heavy_check_mark:                          | N/A                                         |
| `ConversationStartTimeUnixSecs`             | `int64`                                     | :heavy_check_mark:                          | N/A                                         |