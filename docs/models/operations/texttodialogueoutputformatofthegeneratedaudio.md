# TextToDialogueOutputFormatOfTheGeneratedAudio

Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM and WAV formats with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs.


## Supported Types

### TextToDialogueNonStreamingOutputFormats

```go
textToDialogueOutputFormatOfTheGeneratedAudio := operations.CreateTextToDialogueOutputFormatOfTheGeneratedAudioTextToDialogueNonStreamingOutputFormats(operations.TextToDialogueNonStreamingOutputFormats{/* values here */})
```

### TextToDialogueAllowedOutputFormats

```go
textToDialogueOutputFormatOfTheGeneratedAudio := operations.CreateTextToDialogueOutputFormatOfTheGeneratedAudioTextToDialogueAllowedOutputFormats(operations.TextToDialogueAllowedOutputFormats{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch textToDialogueOutputFormatOfTheGeneratedAudio.Type {
	case operations.TextToDialogueOutputFormatOfTheGeneratedAudioTypeTextToDialogueNonStreamingOutputFormats:
		// textToDialogueOutputFormatOfTheGeneratedAudio.TextToDialogueNonStreamingOutputFormats is populated
	case operations.TextToDialogueOutputFormatOfTheGeneratedAudioTypeTextToDialogueAllowedOutputFormats:
		// textToDialogueOutputFormatOfTheGeneratedAudio.TextToDialogueAllowedOutputFormats is populated
}
```
