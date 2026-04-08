# SpellingPatience

Controls if the agent should be more patient when user is spelling numbers and named entities.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SpellingPatienceAuto

// Open enum: custom values can be created with a direct type cast
custom := components.SpellingPatience("custom_value")
```


## Values

| Name                   | Value                  |
| ---------------------- | ---------------------- |
| `SpellingPatienceAuto` | auto                   |
| `SpellingPatienceOff`  | off                    |