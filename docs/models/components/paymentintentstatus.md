# PaymentIntentStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.PaymentIntentStatusCanceled

// Open enum: custom values can be created with a direct type cast
custom := components.PaymentIntentStatus("custom_value")
```


## Values

| Name                                       | Value                                      |
| ------------------------------------------ | ------------------------------------------ |
| `PaymentIntentStatusCanceled`              | canceled                                   |
| `PaymentIntentStatusProcessing`            | processing                                 |
| `PaymentIntentStatusRequiresAction`        | requires_action                            |
| `PaymentIntentStatusRequiresCapture`       | requires_capture                           |
| `PaymentIntentStatusRequiresConfirmation`  | requires_confirmation                      |
| `PaymentIntentStatusRequiresPaymentMethod` | requires_payment_method                    |
| `PaymentIntentStatusSucceeded`             | succeeded                                  |