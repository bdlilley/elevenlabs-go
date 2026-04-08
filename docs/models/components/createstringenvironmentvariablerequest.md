# CreateStringEnvironmentVariableRequest


## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `Type`                                                      | `string`                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `Label`                                                     | `string`                                                    | :heavy_check_mark:                                          | Unique label for the environment variable.                  |
| `Values`                                                    | map[string]`string`                                         | :heavy_check_mark:                                          | Environment-specific values. Must include 'production' key. |