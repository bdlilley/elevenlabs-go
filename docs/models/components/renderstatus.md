# RenderStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.RenderStatusComplete

// Open enum: custom values can be created with a direct type cast
custom := components.RenderStatus("custom_value")
```


## Values

| Name                     | Value                    |
| ------------------------ | ------------------------ |
| `RenderStatusComplete`   | complete                 |
| `RenderStatusProcessing` | processing               |
| `RenderStatusFailed`     | failed                   |