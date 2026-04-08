# TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp32205032
```


## Values

| Name                                                                          | Value                                                                         |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                                  |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                                  |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                                  |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                                  |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                                  |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                                 |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                                 |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                                      |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                                     |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                                 |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                                 |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                                 |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                                |
| `TextToSpeechStreamWithTimestampsOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                                |