# ProjectSnapshotResponseModel


## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `ProjectSnapshotID`                                 | `string`                                            | :heavy_check_mark:                                  | The ID of the project snapshot.                     |
| `ProjectID`                                         | `string`                                            | :heavy_check_mark:                                  | The ID of the project.                              |
| `CreatedAtUnix`                                     | `int64`                                             | :heavy_check_mark:                                  | The creation date of the project snapshot.          |
| `Name`                                              | `string`                                            | :heavy_check_mark:                                  | The name of the project snapshot.                   |
| `AudioUpload`                                       | optionalnullable.OptionalNullable[map[string]`any`] | :heavy_minus_sign:                                  | (Deprecated)                                        |
| `ZipUpload`                                         | optionalnullable.OptionalNullable[map[string]`any`] | :heavy_minus_sign:                                  | (Deprecated)                                        |