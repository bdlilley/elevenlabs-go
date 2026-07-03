# LockReason

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.LockReasonTrialEnded

// Open enum: custom values can be created with a direct type cast
custom := components.LockReason("custom_value")
```


## Values

| Name                              | Value                             |
| --------------------------------- | --------------------------------- |
| `LockReasonTrialEnded`            | trial_ended                       |
| `LockReasonSubscriptionDowngrade` | subscription_downgrade            |
| `LockReasonExposedPublicly`       | exposed_publicly                  |
| `LockReasonSelfDisabled`          | self_disabled                     |