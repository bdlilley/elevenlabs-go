# InteractionBudget

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.InteractionBudgetRealtime

// Open enum: custom values can be created with a direct type cast
custom := components.InteractionBudget("custom_value")
```


## Values

| Name                           | Value                          |
| ------------------------------ | ------------------------------ |
| `InteractionBudgetRealtime`    | realtime                       |
| `InteractionBudgetFiveMinutes` | 5_minutes                      |
| `InteractionBudgetTenMinutes`  | 10_minutes                     |
| `InteractionBudgetOneHour`     | 1_hour                         |