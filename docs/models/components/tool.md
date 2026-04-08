# Tool

Definition for a tool the client can call.


## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `Name`                                                                    | `string`                                                                  | :heavy_check_mark:                                                        | N/A                                                                       |
| `Title`                                                                   | `*string`                                                                 | :heavy_minus_sign:                                                        | N/A                                                                       |
| `Description`                                                             | `*string`                                                                 | :heavy_minus_sign:                                                        | N/A                                                                       |
| `InputSchema`                                                             | map[string]`any`                                                          | :heavy_check_mark:                                                        | N/A                                                                       |
| `OutputSchema`                                                            | map[string]`any`                                                          | :heavy_minus_sign:                                                        | N/A                                                                       |
| `Annotations`                                                             | [*components.ToolAnnotations](../../models/components/toolannotations.md) | :heavy_minus_sign:                                                        | N/A                                                                       |
| `Meta`                                                                    | map[string]`any`                                                          | :heavy_minus_sign:                                                        | N/A                                                                       |
| `AdditionalProperties`                                                    | map[string]`any`                                                          | :heavy_minus_sign:                                                        | N/A                                                                       |