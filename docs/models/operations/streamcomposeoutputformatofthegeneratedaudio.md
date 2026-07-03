# StreamComposeOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models. 

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.StreamComposeOutputFormatOfTheGeneratedAudioAuto
```


## Values

| Name                                                       | Value                                                      |
| ---------------------------------------------------------- | ---------------------------------------------------------- |
| `StreamComposeOutputFormatOfTheGeneratedAudioAuto`         | auto                                                       |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp348000128`  | mp3_48000_128                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp348000192`  | mp3_48000_192                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp348000240`  | mp3_48000_240                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp348000320`  | mp3_48000_320                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                               |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                               |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                               |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                               |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                               |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                   |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                  |
| `StreamComposeOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                              |
| `StreamComposeOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                             |
| `StreamComposeOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                             |