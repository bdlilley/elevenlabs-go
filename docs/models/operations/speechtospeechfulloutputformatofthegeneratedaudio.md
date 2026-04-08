# SpeechToSpeechFullOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp32205032
```


## Values

| Name                                                            | Value                                                           |
| --------------------------------------------------------------- | --------------------------------------------------------------- |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                    |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                    |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                    |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                    |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                    |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                   |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                   |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                        |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                       |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                   |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                   |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                   |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                  |
| `SpeechToSpeechFullOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                  |