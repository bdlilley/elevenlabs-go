# ModelRatesResponseModel


## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `CharacterCostMultiplier`                                                     | `float64`                                                                     | :heavy_check_mark:                                                            | The cost multiplier for characters.                                           |
| `CostDiscountMultiplier`                                                      | `*float64`                                                                    | :heavy_minus_sign:                                                            | Discount multiplier applied to cost estimates. Defaults to 1.0 (no discount). |