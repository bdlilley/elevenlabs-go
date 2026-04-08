# ResponseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGet

Successful Response


## Supported Types

### DubbingTranscriptResponseModel

```go
responseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGet := operations.CreateResponseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGetDubbingTranscriptResponseModel(components.DubbingTranscriptResponseModel{/* values here */})
```

### 

```go
responseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGet := operations.CreateResponseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGetStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGet.Type {
	case operations.ResponseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGetTypeDubbingTranscriptResponseModel:
		// responseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGet.DubbingTranscriptResponseModel is populated
	case operations.ResponseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGetTypeStr:
		// responseGetDubbedTranscriptV1DubbingDubbingIDTranscriptLanguageCodeGet.Str is populated
}
```
