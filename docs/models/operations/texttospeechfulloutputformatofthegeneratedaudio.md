# TextToSpeechFullOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM and WAV formats with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.TextToSpeechFullOutputFormatOfTheGeneratedAudioAlaw8000
```


## Values

| Name                                                          | Value                                                         |
| ------------------------------------------------------------- | ------------------------------------------------------------- |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                  |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                  |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                 |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                 |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                  |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                  |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                  |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                 |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                 |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                 |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                      |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav16000`     | wav_16000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav22050`     | wav_22050                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav24000`     | wav_24000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav32000`     | wav_32000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav44100`     | wav_44100                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav48000`     | wav_48000                                                     |
| `TextToSpeechFullOutputFormatOfTheGeneratedAudioWav8000`      | wav_8000                                                      |