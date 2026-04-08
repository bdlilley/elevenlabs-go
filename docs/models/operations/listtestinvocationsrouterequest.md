# ListTestInvocationsRouteRequest


## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `AgentID`                                                                | `string`                                                                 | :heavy_check_mark:                                                       | Filter by agent ID                                                       |
| `PageSize`                                                               | `*int64`                                                                 | :heavy_minus_sign:                                                       | How many Tests to return at maximum. Can not exceed 100, defaults to 30. |
| `Cursor`                                                                 | `*string`                                                                | :heavy_minus_sign:                                                       | Used for fetching next page. Cursor is returned in the response.         |