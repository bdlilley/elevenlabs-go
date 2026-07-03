# ListConversationTagsRouteRequest


## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `PageSize`                                                       | `*int64`                                                         | :heavy_minus_sign:                                               | How many conversation tags to return. Can not exceed 100.        |
| `Cursor`                                                         | `*string`                                                        | :heavy_minus_sign:                                               | Used for fetching next page. Cursor is returned in the response. |