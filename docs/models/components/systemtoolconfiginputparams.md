# SystemToolConfigInputParams


## Supported Types

### EndCallToolConfig

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsEndCall(components.EndCallToolConfig{/* values here */})
```

### LanguageDetectionToolConfig

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsLanguageDetection(components.LanguageDetectionToolConfig{/* values here */})
```

### PlayDTMFToolConfig

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsPlayKeypadTouchTone(components.PlayDTMFToolConfig{/* values here */})
```

### SkipTurnToolConfig

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsSkipTurn(components.SkipTurnToolConfig{/* values here */})
```

### TransferToAgentToolConfig

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsTransferToAgent(components.TransferToAgentToolConfig{/* values here */})
```

### TransferToNumberToolConfigInput

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsTransferToNumber(components.TransferToNumberToolConfigInput{/* values here */})
```

### VoicemailDetectionToolConfig

```go
systemToolConfigInputParams := components.CreateSystemToolConfigInputParamsVoicemailDetection(components.VoicemailDetectionToolConfig{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch systemToolConfigInputParams.Type {
	case components.SystemToolConfigInputParamsTypeEndCall:
		// systemToolConfigInputParams.EndCallToolConfig is populated
	case components.SystemToolConfigInputParamsTypeLanguageDetection:
		// systemToolConfigInputParams.LanguageDetectionToolConfig is populated
	case components.SystemToolConfigInputParamsTypePlayKeypadTouchTone:
		// systemToolConfigInputParams.PlayDTMFToolConfig is populated
	case components.SystemToolConfigInputParamsTypeSkipTurn:
		// systemToolConfigInputParams.SkipTurnToolConfig is populated
	case components.SystemToolConfigInputParamsTypeTransferToAgent:
		// systemToolConfigInputParams.TransferToAgentToolConfig is populated
	case components.SystemToolConfigInputParamsTypeTransferToNumber:
		// systemToolConfigInputParams.TransferToNumberToolConfigInput is populated
	case components.SystemToolConfigInputParamsTypeVoicemailDetection:
		// systemToolConfigInputParams.VoicemailDetectionToolConfig is populated
}
```
