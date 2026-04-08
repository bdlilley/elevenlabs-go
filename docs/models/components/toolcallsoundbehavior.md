# ToolCallSoundBehavior

Determines how the tool call sound should be played.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ToolCallSoundBehaviorAuto

// Open enum: custom values can be created with a direct type cast
custom := components.ToolCallSoundBehavior("custom_value")
```


## Values

| Name                          | Value                         |
| ----------------------------- | ----------------------------- |
| `ToolCallSoundBehaviorAuto`   | auto                          |
| `ToolCallSoundBehaviorAlways` | always                        |