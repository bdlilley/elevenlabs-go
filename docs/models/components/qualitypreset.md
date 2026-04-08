# QualityPreset

The quality preset level of the project.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.QualityPresetStandard

// Open enum: custom values can be created with a direct type cast
custom := components.QualityPreset("custom_value")
```


## Values

| Name                         | Value                        |
| ---------------------------- | ---------------------------- |
| `QualityPresetStandard`      | standard                     |
| `QualityPresetHigh`          | high                         |
| `QualityPresetHighest`       | highest                      |
| `QualityPresetUltra`         | ultra                        |
| `QualityPresetUltraLossless` | ultra_lossless               |