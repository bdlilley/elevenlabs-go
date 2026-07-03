# WebhookHMACSettings

Settings for creating an HMAC-authenticated webhook


## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `AuthType`                                                                | `string`                                                                  | :heavy_check_mark:                                                        | The authentication type for this webhook                                  |
| `Name`                                                                    | `string`                                                                  | :heavy_check_mark:                                                        | The display name for this webhook                                         |
| `WebhookURL`                                                              | `string`                                                                  | :heavy_check_mark:                                                        | The HTTPS callback URL that will be called when this webhook is triggered |
| `RequestHeaders`                                                          | map[string]`string`                                                       | :heavy_minus_sign:                                                        | Optional custom request headers to include with each webhook delivery     |