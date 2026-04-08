# TextToSpeechStreamOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp32205032
```


## Values

| Name                                                            | Value                                                           |
| --------------------------------------------------------------- | --------------------------------------------------------------- |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                    |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                    |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                    |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                    |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                    |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                   |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                   |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                        |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                       |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                   |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                   |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                   |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                  |
| `TextToSpeechStreamOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                  |