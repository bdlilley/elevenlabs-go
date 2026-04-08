# TestRunStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.TestRunStatusPending

// Open enum: custom values can be created with a direct type cast
custom := components.TestRunStatus("custom_value")
```


## Values

| Name                   | Value                  |
| ---------------------- | ---------------------- |
| `TestRunStatusPending` | pending                |
| `TestRunStatusPassed`  | passed                 |
| `TestRunStatusFailed`  | failed                 |