# Verbosity

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.VerbosityAuto

// Open enum: custom values can be created with a direct type cast
custom := components.Verbosity("custom_value")
```


## Values

| Name                | Value               |
| ------------------- | ------------------- |
| `VerbosityAuto`     | auto                |
| `VerbosityConcise`  | concise             |
| `VerbosityThorough` | thorough            |