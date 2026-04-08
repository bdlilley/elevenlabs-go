# PaymentIntentStatuss

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.PaymentIntentStatussCanceled

// Open enum: custom values can be created with a direct type cast
custom := components.PaymentIntentStatuss("custom_value")
```


## Values

| Name                                        | Value                                       |
| ------------------------------------------- | ------------------------------------------- |
| `PaymentIntentStatussCanceled`              | canceled                                    |
| `PaymentIntentStatussProcessing`            | processing                                  |
| `PaymentIntentStatussRequiresAction`        | requires_action                             |
| `PaymentIntentStatussRequiresCapture`       | requires_capture                            |
| `PaymentIntentStatussRequiresConfirmation`  | requires_confirmation                       |
| `PaymentIntentStatussRequiresPaymentMethod` | requires_payment_method                     |
| `PaymentIntentStatussSucceeded`             | succeeded                                   |