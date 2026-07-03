# AudioFilterID

Identifiers for audio voice filters.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AudioFilterIDPhone

// Open enum: custom values can be created with a direct type cast
custom := components.AudioFilterID("custom_value")
```


## Values

| Name                           | Value                          |
| ------------------------------ | ------------------------------ |
| `AudioFilterIDPhone`           | phone                          |
| `AudioFilterIDLowQualityPhone` | low_quality_phone              |
| `AudioFilterIDBrightPhone`     | bright_phone                   |