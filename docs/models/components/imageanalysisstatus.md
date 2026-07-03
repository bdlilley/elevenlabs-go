# ImageAnalysisStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ImageAnalysisStatusProcessing

// Open enum: custom values can be created with a direct type cast
custom := components.ImageAnalysisStatus("custom_value")
```


## Values

| Name                            | Value                           |
| ------------------------------- | ------------------------------- |
| `ImageAnalysisStatusProcessing` | processing                      |
| `ImageAnalysisStatusCompleted`  | completed                       |
| `ImageAnalysisStatusFailed`     | failed                          |