# SystemToolConfigOutputParams


## Supported Types

### EndCallToolConfig

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsEndCall(components.EndCallToolConfig{/* values here */})
```

### LanguageDetectionToolConfig

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsLanguageDetection(components.LanguageDetectionToolConfig{/* values here */})
```

### PlayDTMFToolConfig

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsPlayKeypadTouchTone(components.PlayDTMFToolConfig{/* values here */})
```

### SkipTurnToolConfig

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsSkipTurn(components.SkipTurnToolConfig{/* values here */})
```

### TransferToAgentToolConfig

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsTransferToAgent(components.TransferToAgentToolConfig{/* values here */})
```

### TransferToNumberToolConfigOutput

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsTransferToNumber(components.TransferToNumberToolConfigOutput{/* values here */})
```

### VoicemailDetectionToolConfig

```go
systemToolConfigOutputParams := components.CreateSystemToolConfigOutputParamsVoicemailDetection(components.VoicemailDetectionToolConfig{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch systemToolConfigOutputParams.Type {
	case components.SystemToolConfigOutputParamsTypeEndCall:
		// systemToolConfigOutputParams.EndCallToolConfig is populated
	case components.SystemToolConfigOutputParamsTypeLanguageDetection:
		// systemToolConfigOutputParams.LanguageDetectionToolConfig is populated
	case components.SystemToolConfigOutputParamsTypePlayKeypadTouchTone:
		// systemToolConfigOutputParams.PlayDTMFToolConfig is populated
	case components.SystemToolConfigOutputParamsTypeSkipTurn:
		// systemToolConfigOutputParams.SkipTurnToolConfig is populated
	case components.SystemToolConfigOutputParamsTypeTransferToAgent:
		// systemToolConfigOutputParams.TransferToAgentToolConfig is populated
	case components.SystemToolConfigOutputParamsTypeTransferToNumber:
		// systemToolConfigOutputParams.TransferToNumberToolConfigOutput is populated
	case components.SystemToolConfigOutputParamsTypeVoicemailDetection:
		// systemToolConfigOutputParams.VoicemailDetectionToolConfig is populated
}
```
