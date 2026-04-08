# AudioAnalysisStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AudioAnalysisStatusProcessing

// Open enum: custom values can be created with a direct type cast
custom := components.AudioAnalysisStatus("custom_value")
```


## Values

| Name                            | Value                           |
| ------------------------------- | ------------------------------- |
| `AudioAnalysisStatusProcessing` | processing                      |
| `AudioAnalysisStatusCompleted`  | completed                       |
| `AudioAnalysisStatusFailed`     | failed                          |