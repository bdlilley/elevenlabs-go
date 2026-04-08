# GetToolDependentAgentsRouteRequest


## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `ToolID`                                                                     | `string`                                                                     | :heavy_check_mark:                                                           | ID of the requested tool.                                                    |
| `Cursor`                                                                     | optionalnullable.OptionalNullable[`string`]                                  | :heavy_minus_sign:                                                           | Used for fetching next page. Cursor is returned in the response.             |
| `PageSize`                                                                   | `*int64`                                                                     | :heavy_minus_sign:                                                           | How many documents to return at maximum. Can not exceed 100, defaults to 30. |