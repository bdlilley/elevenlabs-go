# GenerateOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models. 

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.GenerateOutputFormatOfTheGeneratedAudioAuto
```


## Values

| Name                                                  | Value                                                 |
| ----------------------------------------------------- | ----------------------------------------------------- |
| `GenerateOutputFormatOfTheGeneratedAudioAuto`         | auto                                                  |
| `GenerateOutputFormatOfTheGeneratedAudioMp348000128`  | mp3_48000_128                                         |
| `GenerateOutputFormatOfTheGeneratedAudioMp348000192`  | mp3_48000_192                                         |
| `GenerateOutputFormatOfTheGeneratedAudioMp348000240`  | mp3_48000_240                                         |
| `GenerateOutputFormatOfTheGeneratedAudioMp348000320`  | mp3_48000_320                                         |
| `GenerateOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                          |
| `GenerateOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                          |
| `GenerateOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                          |
| `GenerateOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                          |
| `GenerateOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                          |
| `GenerateOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                         |
| `GenerateOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                         |
| `GenerateOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                              |
| `GenerateOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                             |
| `GenerateOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                             |
| `GenerateOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                             |
| `GenerateOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                             |
| `GenerateOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                             |
| `GenerateOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                             |
| `GenerateOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                             |
| `GenerateOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                             |
| `GenerateOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                         |
| `GenerateOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                         |
| `GenerateOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                         |
| `GenerateOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                        |
| `GenerateOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                        |