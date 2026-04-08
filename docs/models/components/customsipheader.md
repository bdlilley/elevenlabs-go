# CustomSIPHeader

Custom SIP header for phone transfers with a static (validated) value.


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `Type`                                      | `*string`                                   | :heavy_minus_sign:                          | N/A                                         |
| `Key`                                       | `string`                                    | :heavy_check_mark:                          | The SIP header name (e.g., 'X-Customer-ID') |
| `Value`                                     | `string`                                    | :heavy_check_mark:                          | The header value                            |