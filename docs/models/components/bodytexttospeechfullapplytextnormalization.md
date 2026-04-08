# BodyTextToSpeechFullApplyTextNormalization

This parameter controls text normalization with three modes: 'auto', 'on', and 'off'. When set to 'auto', the system will automatically decide whether to apply text normalization (e.g., spelling out numbers). With 'on', text normalization will always be applied, while with 'off', it will be skipped.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BodyTextToSpeechFullApplyTextNormalizationAuto
```


## Values

| Name                                             | Value                                            |
| ------------------------------------------------ | ------------------------------------------------ |
| `BodyTextToSpeechFullApplyTextNormalizationAuto` | auto                                             |
| `BodyTextToSpeechFullApplyTextNormalizationOn`   | on                                               |
| `BodyTextToSpeechFullApplyTextNormalizationOff`  | off                                              |