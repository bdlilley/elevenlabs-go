# AsyncConversationMetadata

Metadata for async conversation delivery (Zendesk, Slack, etc.).


## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `DeliveryStatus`                                                       | [components.DeliveryStatus](../../models/components/deliverystatus.md) | :heavy_check_mark:                                                     | N/A                                                                    |
| `DeliveryTimestamp`                                                    | `int64`                                                                | :heavy_check_mark:                                                     | N/A                                                                    |
| `DeliveryError`                                                        | `*string`                                                              | :heavy_minus_sign:                                                     | N/A                                                                    |
| `ExternalSystem`                                                       | `string`                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `ExternalID`                                                           | `string`                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `RetryCount`                                                           | `*int64`                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `LastRetryTimestamp`                                                   | `*int64`                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `LastProcessedExternalMessageID`                                       | `*string`                                                              | :heavy_minus_sign:                                                     | N/A                                                                    |