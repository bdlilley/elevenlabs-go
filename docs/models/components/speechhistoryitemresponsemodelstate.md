# SpeechHistoryItemResponseModelState

The state of the history item.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SpeechHistoryItemResponseModelStateCreated

// Open enum: custom values can be created with a direct type cast
custom := components.SpeechHistoryItemResponseModelState("custom_value")
```


## Values

| Name                                            | Value                                           |
| ----------------------------------------------- | ----------------------------------------------- |
| `SpeechHistoryItemResponseModelStateCreated`    | created                                         |
| `SpeechHistoryItemResponseModelStateDeleted`    | deleted                                         |
| `SpeechHistoryItemResponseModelStateProcessing` | processing                                      |