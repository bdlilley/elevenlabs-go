# BatchCallRecipientStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BatchCallRecipientStatusPending

// Open enum: custom values can be created with a direct type cast
custom := components.BatchCallRecipientStatus("custom_value")
```


## Values

| Name                                 | Value                                |
| ------------------------------------ | ------------------------------------ |
| `BatchCallRecipientStatusPending`    | pending                              |
| `BatchCallRecipientStatusDispatched` | dispatched                           |
| `BatchCallRecipientStatusInitiated`  | initiated                            |
| `BatchCallRecipientStatusInProgress` | in_progress                          |
| `BatchCallRecipientStatusCompleted`  | completed                            |
| `BatchCallRecipientStatusFailed`     | failed                               |
| `BatchCallRecipientStatusCancelled`  | cancelled                            |
| `BatchCallRecipientStatusVoicemail`  | voicemail                            |