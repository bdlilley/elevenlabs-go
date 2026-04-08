# TestType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.TestTypeLlm

// Open enum: custom values can be created with a direct type cast
custom := components.TestType("custom_value")
```


## Values

| Name                 | Value                |
| -------------------- | -------------------- |
| `TestTypeLlm`        | llm                  |
| `TestTypeTool`       | tool                 |
| `TestTypeSimulation` | simulation           |
| `TestTypeFolder`     | folder               |