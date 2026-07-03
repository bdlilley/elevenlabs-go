# OrderState

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.OrderStateOpen

// Open enum: custom values can be created with a direct type cast
custom := components.OrderState("custom_value")
```


## Values

| Name                  | Value                 |
| --------------------- | --------------------- |
| `OrderStateOpen`      | open                  |
| `OrderStateSubmitted` | submitted             |
| `OrderStatePaid`      | paid                  |
| `OrderStateAccepted`  | accepted              |
| `OrderStateRejected`  | rejected              |
| `OrderStateDone`      | done                  |