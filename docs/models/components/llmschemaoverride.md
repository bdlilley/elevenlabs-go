# LLMSchemaOverride


## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `Source`                                                                               | `*string`                                                                              | :heavy_minus_sign:                                                                     | N/A                                                                                    |
| `Prompt`                                                                               | optionalnullable.OptionalNullable[`string`]                                            | :heavy_minus_sign:                                                                     | Prompt override for the LLM. If not provided, the original schema description is used. |