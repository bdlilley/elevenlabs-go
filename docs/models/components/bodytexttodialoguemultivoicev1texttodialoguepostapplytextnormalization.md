# BodyTextToDialogueMultiVoiceV1TextToDialoguePostApplyTextNormalization

This parameter controls text normalization with three modes: 'auto', 'on', and 'off'. When set to 'auto', the system will automatically decide whether to apply text normalization (e.g., spelling out numbers). With 'on', text normalization will always be applied, while with 'off', it will be skipped.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BodyTextToDialogueMultiVoiceV1TextToDialoguePostApplyTextNormalizationAuto
```


## Values

| Name                                                                         | Value                                                                        |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `BodyTextToDialogueMultiVoiceV1TextToDialoguePostApplyTextNormalizationAuto` | auto                                                                         |
| `BodyTextToDialogueMultiVoiceV1TextToDialoguePostApplyTextNormalizationOn`   | on                                                                           |
| `BodyTextToDialogueMultiVoiceV1TextToDialoguePostApplyTextNormalizationOff`  | off                                                                          |