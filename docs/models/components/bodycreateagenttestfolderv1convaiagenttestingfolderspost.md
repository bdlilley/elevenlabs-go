# BodyCreateAgentTestFolderV1ConvaiAgentTestingFoldersPost


## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `Name`                                                                                      | `string`                                                                                    | :heavy_check_mark:                                                                          | The name of the folder to create                                                            |
| `ParentFolderID`                                                                            | optionalnullable.OptionalNullable[`string`]                                                 | :heavy_minus_sign:                                                                          | The ID of the parent folder. If not provided, the folder will be created at the root level. |