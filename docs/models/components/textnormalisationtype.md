# TextNormalisationType

Method for converting numbers to words before sending to TTS

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.TextNormalisationTypeSystemPrompt

// Open enum: custom values can be created with a direct type cast
custom := components.TextNormalisationType("custom_value")
```


## Values

| Name                                | Value                               |
| ----------------------------------- | ----------------------------------- |
| `TextNormalisationTypeSystemPrompt` | system_prompt                       |
| `TextNormalisationTypeElevenlabs`   | elevenlabs                          |