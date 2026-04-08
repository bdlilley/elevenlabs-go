# BodySpeechToTextV1SpeechToTextPostFileFormat

The format of input audio. Options are 'pcm_s16le_16' or 'other' For `pcm_s16le_16`, the input audio must be 16-bit PCM at a 16kHz sample rate, single channel (mono), and little-endian byte order. Latency will be lower than with passing an encoded waveform.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BodySpeechToTextV1SpeechToTextPostFileFormatPcmS16le16
```


## Values

| Name                                                     | Value                                                    |
| -------------------------------------------------------- | -------------------------------------------------------- |
| `BodySpeechToTextV1SpeechToTextPostFileFormatPcmS16le16` | pcm_s16le_16                                             |
| `BodySpeechToTextV1SpeechToTextPostFileFormatOther`      | other                                                    |