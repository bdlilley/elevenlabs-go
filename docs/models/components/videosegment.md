# VideoSegment


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `StartMs`                                   | `int64`                                     | :heavy_check_mark:                          | N/A                                         |
| `EndMs`                                     | `int64`                                     | :heavy_check_mark:                          | N/A                                         |
| `Description`                               | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `Subjects`                                  | []`string`                                  | :heavy_minus_sign:                          | N/A                                         |
| `ShotType`                                  | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |
| `CameraMovement`                            | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |
| `TransitionIn`                              | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |
| `HasSpeech`                                 | `*bool`                                     | :heavy_minus_sign:                          | N/A                                         |
| `HasMusic`                                  | `*bool`                                     | :heavy_minus_sign:                          | N/A                                         |
| `Pacing`                                    | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | N/A                                         |