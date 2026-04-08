# SpeechToTextWordResponseModelType

The type of the word or sound. 'audio_event' is used for non-word sounds like laughter or footsteps.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SpeechToTextWordResponseModelTypeWord

// Open enum: custom values can be created with a direct type cast
custom := components.SpeechToTextWordResponseModelType("custom_value")
```


## Values

| Name                                          | Value                                         |
| --------------------------------------------- | --------------------------------------------- |
| `SpeechToTextWordResponseModelTypeWord`       | word                                          |
| `SpeechToTextWordResponseModelTypeSpacing`    | spacing                                       |
| `SpeechToTextWordResponseModelTypeAudioEvent` | audio_event                                   |