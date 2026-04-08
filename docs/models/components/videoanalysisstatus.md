# VideoAnalysisStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.VideoAnalysisStatusProcessing

// Open enum: custom values can be created with a direct type cast
custom := components.VideoAnalysisStatus("custom_value")
```


## Values

| Name                            | Value                           |
| ------------------------------- | ------------------------------- |
| `VideoAnalysisStatusProcessing` | processing                      |
| `VideoAnalysisStatusCompleted`  | completed                       |
| `VideoAnalysisStatusFailed`     | failed                          |