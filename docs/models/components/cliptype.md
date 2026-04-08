# ClipType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ClipTypeVideo

// Open enum: custom values can be created with a direct type cast
custom := components.ClipType("custom_value")
```


## Values

| Name                    | Value                   |
| ----------------------- | ----------------------- |
| `ClipTypeVideo`         | video                   |
| `ClipTypeImage`         | image                   |
| `ClipTypeExternalAudio` | external_audio          |
| `ClipTypeTtsNode`       | tts_node                |