# ExternalFolderSyncInfo

Metadata for a KB folder that mirrors an external source folder.


## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `Type`                                                                     | [components.ExternalSyncType](../../models/components/externalsynctype.md) | :heavy_check_mark:                                                         | N/A                                                                        |
| `SourceEntityID`                                                           | `string`                                                                   | :heavy_check_mark:                                                         | Entity ID in the external system                                           |
| `IntegrationConnectionID`                                                  | `string`                                                                   | :heavy_check_mark:                                                         | Integration connection instance ID                                         |
| `RootFolderID`                                                             | `*string`                                                                  | :heavy_minus_sign:                                                         | KB folder ID of the sync root. None means this folder is the root.         |
| `SyncCursor`                                                               | `*string`                                                                  | :heavy_minus_sign:                                                         | Opaque cursor for incremental sync, interpreted by the provider            |
| `LastSyncAt`                                                               | `*int64`                                                                   | :heavy_minus_sign:                                                         | Unix timestamp of last completed sync                                      |