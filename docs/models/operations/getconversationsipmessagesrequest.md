# GetConversationSipMessagesRequest


## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `ConversationID`                                                 | `string`                                                         | :heavy_check_mark:                                               | The id of the conversation you're taking the action on.          | 21m00Tcm4TlvDq8ikWAM                                             |
| `PageSize`                                                       | `*int64`                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `Cursor`                                                         | `*string`                                                        | :heavy_minus_sign:                                               | Used for fetching next page. Cursor is returned in the response. |                                                                  |