# WorkflowResultConditionModelOutput


## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `Label`                                                                            | `*string`                                                                          | :heavy_check_mark:                                                                 | Optional human-readable label for the condition used throughout the UI.            |
| `Type`                                                                             | `*string`                                                                          | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `Successful`                                                                       | `bool`                                                                             | :heavy_check_mark:                                                                 | Whether all tools in the previously executed tool node were executed successfully. |