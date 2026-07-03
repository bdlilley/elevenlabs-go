# ComposeDetailedOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models. 

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.ComposeDetailedOutputFormatOfTheGeneratedAudioAuto
```


## Values

| Name                                                         | Value                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioAuto`         | auto                                                         |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp348000128`  | mp3_48000_128                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp348000192`  | mp3_48000_192                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp348000240`  | mp3_48000_240                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp348000320`  | mp3_48000_320                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                 |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                 |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                 |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                 |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                 |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                     |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                    |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                               |
| `ComposeDetailedOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                               |