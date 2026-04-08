# SpeakerSeparationResponseModelStatus

The status of the speaker separation.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SpeakerSeparationResponseModelStatusNotStarted

// Open enum: custom values can be created with a direct type cast
custom := components.SpeakerSeparationResponseModelStatus("custom_value")
```


## Values

| Name                                             | Value                                            |
| ------------------------------------------------ | ------------------------------------------------ |
| `SpeakerSeparationResponseModelStatusNotStarted` | not_started                                      |
| `SpeakerSeparationResponseModelStatusPending`    | pending                                          |
| `SpeakerSeparationResponseModelStatusCompleted`  | completed                                        |
| `SpeakerSeparationResponseModelStatusFailed`     | failed                                           |