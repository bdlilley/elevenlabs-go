# DeliveryStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.DeliveryStatusPending

// Open enum: custom values can be created with a direct type cast
custom := components.DeliveryStatus("custom_value")
```


## Values

| Name                    | Value                   |
| ----------------------- | ----------------------- |
| `DeliveryStatusPending` | pending                 |
| `DeliveryStatusSuccess` | success                 |
| `DeliveryStatusFailed`  | failed                  |