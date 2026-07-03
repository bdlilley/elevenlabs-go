# SpeechEngineConfigRequestHeaders


## Supported Types

### 

```go
speechEngineConfigRequestHeaders := components.CreateSpeechEngineConfigRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
speechEngineConfigRequestHeaders := components.CreateSpeechEngineConfigRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
speechEngineConfigRequestHeaders := components.CreateSpeechEngineConfigRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch speechEngineConfigRequestHeaders.Type {
	case components.SpeechEngineConfigRequestHeadersTypeStr:
		// speechEngineConfigRequestHeaders.Str is populated
	case components.SpeechEngineConfigRequestHeadersTypeConvAISecretLocator:
		// speechEngineConfigRequestHeaders.ConvAISecretLocator is populated
	case components.SpeechEngineConfigRequestHeadersTypeConvAIDynamicVariable:
		// speechEngineConfigRequestHeaders.ConvAIDynamicVariable is populated
}
```
