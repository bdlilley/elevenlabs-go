# UpsertOrderItemRequest


## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `Item`                                                                               | [components.OrderItemRequestInput](../../models/components/orderitemrequestinput.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `ItemID`                                                                             | `*string`                                                                            | :heavy_minus_sign:                                                                   | The ID of an existing item to update. Omit to create a new item.                     |