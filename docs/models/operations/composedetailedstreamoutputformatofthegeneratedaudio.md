# ComposeDetailedStreamOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models. 

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.ComposeDetailedStreamOutputFormatOfTheGeneratedAudioAuto
```


## Values

| Name                                                               | Value                                                              |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioAuto`         | auto                                                               |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp348000128`  | mp3_48000_128                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp348000192`  | mp3_48000_192                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp348000240`  | mp3_48000_240                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp348000320`  | mp3_48000_320                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                       |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                       |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                       |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                       |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                       |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                           |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                          |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                      |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                     |
| `ComposeDetailedStreamOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                     |