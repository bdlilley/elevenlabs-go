# PayoutType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.PayoutTypeNone

// Open enum: custom values can be created with a direct type cast
custom := components.PayoutType("custom_value")
```


## Values

| Name                        | Value                       |
| --------------------------- | --------------------------- |
| `PayoutTypeNone`            | none                        |
| `PayoutTypeEngagementBased` | engagement_based            |
| `PayoutTypeFixedPayout`     | fixed_payout                |