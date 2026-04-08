# ToolExecutionMode

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ToolExecutionModeImmediate

// Open enum: custom values can be created with a direct type cast
custom := components.ToolExecutionMode("custom_value")
```


## Values

| Name                              | Value                             |
| --------------------------------- | --------------------------------- |
| `ToolExecutionModeImmediate`      | immediate                         |
| `ToolExecutionModePostToolSpeech` | post_tool_speech                  |
| `ToolExecutionModeAsync`          | async                             |