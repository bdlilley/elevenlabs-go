# ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGet

The transcript data


## Supported Types

### SpeechToTextChunkResponseModel

```go
responseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet := operations.CreateResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGetSpeechToTextChunkResponseModel(components.SpeechToTextChunkResponseModel{/* values here */})
```

### MultichannelSpeechToTextResponseModel

```go
responseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet := operations.CreateResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGetMultichannelSpeechToTextResponseModel(components.MultichannelSpeechToTextResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet.Type {
	case operations.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGetTypeSpeechToTextChunkResponseModel:
		// responseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet.SpeechToTextChunkResponseModel is populated
	case operations.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGetTypeMultichannelSpeechToTextResponseModel:
		// responseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet.MultichannelSpeechToTextResponseModel is populated
	default:
		// Unknown type - use responseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet.GetUnknownRaw() for raw JSON
}
```
