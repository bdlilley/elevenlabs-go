# ToolInterruptionMode

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ToolInterruptionModeAllow

// Open enum: custom values can be created with a direct type cast
custom := components.ToolInterruptionMode("custom_value")
```


## Values

| Name                                           | Value                                          |
| ---------------------------------------------- | ---------------------------------------------- |
| `ToolInterruptionModeAllow`                    | allow                                          |
| `ToolInterruptionModeDisableDuringTool`        | disable_during_tool                            |
| `ToolInterruptionModeDisableDuringToolAndTurn` | disable_during_tool_and_turn                   |