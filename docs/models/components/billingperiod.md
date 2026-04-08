# BillingPeriod

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BillingPeriodMonthlyPeriod

// Open enum: custom values can be created with a direct type cast
custom := components.BillingPeriod("custom_value")
```


## Values

| Name                            | Value                           |
| ------------------------------- | ------------------------------- |
| `BillingPeriodMonthlyPeriod`    | monthly_period                  |
| `BillingPeriodThreeMonthPeriod` | 3_month_period                  |
| `BillingPeriodSixMonthPeriod`   | 6_month_period                  |
| `BillingPeriodAnnualPeriod`     | annual_period                   |