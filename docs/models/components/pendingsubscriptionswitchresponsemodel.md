# PendingSubscriptionSwitchResponseModel


## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `Kind`                                                               | `*string`                                                            | :heavy_minus_sign:                                                   | N/A                                                                  |
| `NextTier`                                                           | [components.NextTier](../../models/components/nexttier.md)           | :heavy_check_mark:                                                   | The tier to change to.                                               |
| `NextBillingPeriod`                                                  | [components.BillingPeriod](../../models/components/billingperiod.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `TimestampSeconds`                                                   | `int64`                                                              | :heavy_check_mark:                                                   | The timestamp of the change.                                         |