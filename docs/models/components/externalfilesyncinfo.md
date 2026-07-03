# ExternalFileSyncInfo

Tracks the link back to the original file in an external source.


## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `Type`                                                                      | [components.ExternalSyncType](../../models/components/externalsynctype.md)  | :heavy_check_mark:                                                          | N/A                                                                         |
| `SourceEntityID`                                                            | `string`                                                                    | :heavy_check_mark:                                                          | Entity ID in the external system                                            |
| `IntegrationConnectionID`                                                   | `string`                                                                    | :heavy_check_mark:                                                          | Integration connection instance ID                                          |
| `SourceParentEntityID`                                                      | `string`                                                                    | :heavy_check_mark:                                                          | Folder ID in the external system this file was synced from                  |
| `SourceMimeType`                                                            | `string`                                                                    | :heavy_check_mark:                                                          | Original MIME type in the external system                                   |
| `SourceModifiedTime`                                                        | [time.Time](https://pkg.go.dev/time#Time)                                   | :heavy_check_mark:                                                          | Last modified time from the external system                                 |
| `RootFolderID`                                                              | `*string`                                                                   | :heavy_minus_sign:                                                          | KB folder ID of the sync root, used to query all entities under a sync tree |