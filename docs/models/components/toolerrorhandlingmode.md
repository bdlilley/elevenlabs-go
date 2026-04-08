# ToolErrorHandlingMode

Controls how tool errors are processed before being shared with the agent.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ToolErrorHandlingModeAuto

// Open enum: custom values can be created with a direct type cast
custom := components.ToolErrorHandlingMode("custom_value")
```


## Values

| Name                               | Value                              |
| ---------------------------------- | ---------------------------------- |
| `ToolErrorHandlingModeAuto`        | auto                               |
| `ToolErrorHandlingModeSummarized`  | summarized                         |
| `ToolErrorHandlingModePassthrough` | passthrough                        |
| `ToolErrorHandlingModeHide`        | hide                               |