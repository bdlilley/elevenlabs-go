# SubmitOrderResponse


## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `OrderID`                                                      | `string`                                                       | :heavy_check_mark:                                             | N/A                                                            |
| `State`                                                        | [components.OrderState](../../models/components/orderstate.md) | :heavy_check_mark:                                             | N/A                                                            |
| `SubmittedAt`                                                  | [time.Time](https://pkg.go.dev/time#Time)                      | :heavy_check_mark:                                             | The timestamp when the order was submitted.                    |