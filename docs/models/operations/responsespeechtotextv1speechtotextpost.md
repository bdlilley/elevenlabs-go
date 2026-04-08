# ResponseSpeechToTextV1SpeechToTextPost

Synchronous transcription result


## Supported Types

### SpeechToTextChunkResponseModel

```go
responseSpeechToTextV1SpeechToTextPost := operations.CreateResponseSpeechToTextV1SpeechToTextPostSpeechToTextChunkResponseModel(components.SpeechToTextChunkResponseModel{/* values here */})
```

### MultichannelSpeechToTextResponseModel

```go
responseSpeechToTextV1SpeechToTextPost := operations.CreateResponseSpeechToTextV1SpeechToTextPostMultichannelSpeechToTextResponseModel(components.MultichannelSpeechToTextResponseModel{/* values here */})
```

### SpeechToTextWebhookResponseModel

```go
responseSpeechToTextV1SpeechToTextPost := operations.CreateResponseSpeechToTextV1SpeechToTextPostSpeechToTextWebhookResponseModel(components.SpeechToTextWebhookResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseSpeechToTextV1SpeechToTextPost.Type {
	case operations.ResponseSpeechToTextV1SpeechToTextPostTypeSpeechToTextChunkResponseModel:
		// responseSpeechToTextV1SpeechToTextPost.SpeechToTextChunkResponseModel is populated
	case operations.ResponseSpeechToTextV1SpeechToTextPostTypeMultichannelSpeechToTextResponseModel:
		// responseSpeechToTextV1SpeechToTextPost.MultichannelSpeechToTextResponseModel is populated
	case operations.ResponseSpeechToTextV1SpeechToTextPostTypeSpeechToTextWebhookResponseModel:
		// responseSpeechToTextV1SpeechToTextPost.SpeechToTextWebhookResponseModel is populated
}
```
