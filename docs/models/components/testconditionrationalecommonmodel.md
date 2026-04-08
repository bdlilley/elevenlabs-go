# TestConditionRationaleCommonModel

Structured rationale for test condition results containing individual failure/success reasons.


## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `Messages`                                                  | []`string`                                                  | :heavy_minus_sign:                                          | List of individual parameter evaluation messages or reasons |
| `Summary`                                                   | `*string`                                                   | :heavy_minus_sign:                                          | High-level summary of the evaluation result                 |