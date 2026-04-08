# ResponseFilterMode

Controls how tool responses are filtered before being visible to the agent.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ResponseFilterModeAll

// Open enum: custom values can be created with a direct type cast
custom := components.ResponseFilterMode("custom_value")
```


## Values

| Name                        | Value                       |
| --------------------------- | --------------------------- |
| `ResponseFilterModeAll`     | all                         |
| `ResponseFilterModeAllow`   | allow                       |
| `ResponseFilterModeHideAll` | hide_all                    |