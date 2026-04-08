# CustomLLMRequestHeaders


## Supported Types

### 

```go
customLLMRequestHeaders := components.CreateCustomLLMRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
customLLMRequestHeaders := components.CreateCustomLLMRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
customLLMRequestHeaders := components.CreateCustomLLMRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

### ConvAIEnvVarLocator

```go
customLLMRequestHeaders := components.CreateCustomLLMRequestHeadersConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch customLLMRequestHeaders.Type {
	case components.CustomLLMRequestHeadersTypeStr:
		// customLLMRequestHeaders.Str is populated
	case components.CustomLLMRequestHeadersTypeConvAISecretLocator:
		// customLLMRequestHeaders.ConvAISecretLocator is populated
	case components.CustomLLMRequestHeadersTypeConvAIDynamicVariable:
		// customLLMRequestHeaders.ConvAIDynamicVariable is populated
	case components.CustomLLMRequestHeadersTypeConvAIEnvVarLocator:
		// customLLMRequestHeaders.ConvAIEnvVarLocator is populated
}
```
