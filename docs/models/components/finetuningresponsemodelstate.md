# FineTuningResponseModelState

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.FineTuningResponseModelStateNotStarted

// Open enum: custom values can be created with a direct type cast
custom := components.FineTuningResponseModelState("custom_value")
```


## Values

| Name                                     | Value                                    |
| ---------------------------------------- | ---------------------------------------- |
| `FineTuningResponseModelStateNotStarted` | not_started                              |
| `FineTuningResponseModelStateQueued`     | queued                                   |
| `FineTuningResponseModelStateFineTuning` | fine_tuning                              |
| `FineTuningResponseModelStateFineTuned`  | fine_tuned                               |
| `FineTuningResponseModelStateFailed`     | failed                                   |
| `FineTuningResponseModelStateDelayed`    | delayed                                  |