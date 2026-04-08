# TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM and WAV formats with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioAlaw8000
```


## Values

| Name                                                                        | Value                                                                       |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioAlaw8000`     | alaw_8000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp32205032`   | mp3_22050_32                                                                |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp32400048`   | mp3_24000_48                                                                |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp344100128`  | mp3_44100_128                                                               |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp344100192`  | mp3_44100_192                                                               |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp34410032`   | mp3_44100_32                                                                |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp34410064`   | mp3_44100_64                                                                |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioMp34410096`   | mp3_44100_96                                                                |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioOpus48000128` | opus_48000_128                                                              |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioOpus48000192` | opus_48000_192                                                              |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioOpus4800032`  | opus_48000_32                                                               |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioOpus4800064`  | opus_48000_64                                                               |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioOpus4800096`  | opus_48000_96                                                               |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm16000`     | pcm_16000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm22050`     | pcm_22050                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm24000`     | pcm_24000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm32000`     | pcm_32000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm44100`     | pcm_44100                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm48000`     | pcm_48000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioPcm8000`      | pcm_8000                                                                    |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioUlaw8000`     | ulaw_8000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav16000`     | wav_16000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav22050`     | wav_22050                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav24000`     | wav_24000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav32000`     | wav_32000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav44100`     | wav_44100                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav48000`     | wav_48000                                                                   |
| `TextToSpeechFullWithTimestampsOutputFormatOfTheGeneratedAudioWav8000`      | wav_8000                                                                    |