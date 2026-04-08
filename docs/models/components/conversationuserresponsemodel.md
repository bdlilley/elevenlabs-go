# ConversationUserResponseModel


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `UserID`                                    | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `LastContactUnixSecs`                       | `int64`                                     | :heavy_check_mark:                          | N/A                                         |
| `FirstContactUnixSecs`                      | `int64`                                     | :heavy_check_mark:                          | N/A                                         |
| `ConversationCount`                         | `int64`                                     | :heavy_check_mark:                          | N/A                                         |
| `LastContactAgentID`                        | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |
| `LastContactConversationID`                 | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `LastContactAgentName`                      | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |