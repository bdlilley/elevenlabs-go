# SpeechToSpeechStreamOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp32205032
```


## Values

| Name                                                              | Value                                                             |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                      |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                      |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                      |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                      |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                      |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                     |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                     |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                          |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                         |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                     |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                     |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                     |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                    |
| `SpeechToSpeechStreamOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                    |