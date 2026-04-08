# BatchCallStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BatchCallStatusPending

// Open enum: custom values can be created with a direct type cast
custom := components.BatchCallStatus("custom_value")
```


## Values

| Name                        | Value                       |
| --------------------------- | --------------------------- |
| `BatchCallStatusPending`    | pending                     |
| `BatchCallStatusInProgress` | in_progress                 |
| `BatchCallStatusCompleted`  | completed                   |
| `BatchCallStatusFailed`     | failed                      |
| `BatchCallStatusCancelled`  | cancelled                   |