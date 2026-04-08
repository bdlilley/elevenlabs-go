# DisplayMode

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.DisplayModeText

// Open enum: custom values can be created with a direct type cast
custom := components.DisplayMode("custom_value")
```


## Values

| Name                       | Value                      |
| -------------------------- | -------------------------- |
| `DisplayModeText`          | text                       |
| `DisplayModeAudioOnly`     | audio-only                 |
| `DisplayModeTextWithAudio` | text-with-audio            |