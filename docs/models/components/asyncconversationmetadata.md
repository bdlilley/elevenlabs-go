# AsyncConversationMetadata

Metadata for async conversation delivery (Zendesk, Slack, etc.).


## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `DeliveryStatus`                                                       | [components.DeliveryStatus](../../models/components/deliverystatus.md) | :heavy_check_mark:                                                     | N/A                                                                    |
| `DeliveryTimestamp`                                                    | `int64`                                                                | :heavy_check_mark:                                                     | N/A                                                                    |
| `DeliveryError`                                                        | optionalnullable.OptionalNullable[`string`]                            | :heavy_minus_sign:                                                     | N/A                                                                    |
| `ExternalSystem`                                                       | `string`                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `ExternalID`                                                           | `string`                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `RetryCount`                                                           | `*int64`                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |
| `LastRetryTimestamp`                                                   | optionalnullable.OptionalNullable[`int64`]                             | :heavy_minus_sign:                                                     | N/A                                                                    |
| `LastProcessedExternalMessageID`                                       | optionalnullable.OptionalNullable[`string`]                            | :heavy_minus_sign:                                                     | N/A                                                                    |