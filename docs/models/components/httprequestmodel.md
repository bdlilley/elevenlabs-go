# HTTPRequestModel

HTTP request details.

Spec: https://schema.ocsf.io/1.6.0/objects/http_request


## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `HTTPMethod`                                                     | `string`                                                         | :heavy_check_mark:                                               | HTTP method (GET, POST, etc.)                                    |
| `URL`                                                            | [components.URLModel](../../models/components/urlmodel.md)       | :heavy_check_mark:                                               | OCSF URL object.<br/><br/>Spec: https://schema.ocsf.io/1.6.0/objects/url |
| `UserAgent`                                                      | `*string`                                                        | :heavy_minus_sign:                                               | User agent string                                                |
| `XForwardedFor`                                                  | []`string`                                                       | :heavy_minus_sign:                                               | X-Forwarded-For header as a list                                 |