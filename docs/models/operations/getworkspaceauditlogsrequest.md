# GetWorkspaceAuditLogsRequest


## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `Limit`                                                      | `*int64`                                                     | :heavy_minus_sign:                                           | Maximum number of entries per page                           |
| `Cursor`                                                     | `*string`                                                    | :heavy_minus_sign:                                           | Cursor for the next page (from previous response)            |
| `TimeFromUnixMs`                                             | `*int64`                                                     | :heavy_minus_sign:                                           | Only include entries at or after this time (ms since epoch)  |
| `TimeToUnixMs`                                               | `*int64`                                                     | :heavy_minus_sign:                                           | Only include entries at or before this time (ms since epoch) |
| `ActorUID`                                                   | `*string`                                                    | :heavy_minus_sign:                                           | Filter by actor user ID                                      |
| `ClassName`                                                  | `*string`                                                    | :heavy_minus_sign:                                           | Filter by OCSF event class name (e.g. Account Change)        |
| `ActivityName`                                               | `*string`                                                    | :heavy_minus_sign:                                           | Filter by audit activity name (e.g. Subscription Creation)   |