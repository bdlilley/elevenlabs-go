# ContextAdherence

How much the model adheres to the context of its surrounding chunks. Low adherence means the model can deviate from the context and be more creative. High adherence means the model will be more consistent with the context.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ContextAdherenceLow

// Open enum: custom values can be created with a direct type cast
custom := components.ContextAdherence("custom_value")
```


## Values

| Name                     | Value                    |
| ------------------------ | ------------------------ |
| `ContextAdherenceLow`    | low                      |
| `ContextAdherenceMedium` | medium                   |
| `ContextAdherenceHigh`   | high                     |