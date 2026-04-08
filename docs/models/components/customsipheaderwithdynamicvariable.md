# CustomSIPHeaderWithDynamicVariable

Custom SIP header for phone transfers with a dynamic variable reference.
The value is a variable name that will be resolved at runtime.
Value is not validated here since it will be substituted with actual value later.


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `Type`                                      | `string`                                    | :heavy_check_mark:                          | N/A                                         |
| `Key`                                       | `string`                                    | :heavy_check_mark:                          | The SIP header name (e.g., 'X-Customer-ID') |
| `Value`                                     | `string`                                    | :heavy_check_mark:                          | The dynamic variable name to resolve        |