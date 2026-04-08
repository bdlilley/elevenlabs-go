# WorkspaceBatchCallsResponse


## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `BatchCalls`                                                                   | [][components.BatchCallResponse](../../models/components/batchcallresponse.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `NextDoc`                                                                      | `*string`                                                                      | :heavy_minus_sign:                                                             | The next document, used to paginate through the batch calls                    |
| `HasMore`                                                                      | `*bool`                                                                        | :heavy_minus_sign:                                                             | Whether there are more batch calls to paginate through                         |