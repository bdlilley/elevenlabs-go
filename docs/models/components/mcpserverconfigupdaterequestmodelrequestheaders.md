# MCPServerConfigUpdateRequestModelRequestHeaders


## Supported Types

### 

```go
mcpServerConfigUpdateRequestModelRequestHeaders := components.CreateMCPServerConfigUpdateRequestModelRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
mcpServerConfigUpdateRequestModelRequestHeaders := components.CreateMCPServerConfigUpdateRequestModelRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
mcpServerConfigUpdateRequestModelRequestHeaders := components.CreateMCPServerConfigUpdateRequestModelRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

### ConvAIEnvVarLocator

```go
mcpServerConfigUpdateRequestModelRequestHeaders := components.CreateMCPServerConfigUpdateRequestModelRequestHeadersConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigUpdateRequestModelRequestHeaders.Type {
	case components.MCPServerConfigUpdateRequestModelRequestHeadersTypeStr:
		// mcpServerConfigUpdateRequestModelRequestHeaders.Str is populated
	case components.MCPServerConfigUpdateRequestModelRequestHeadersTypeConvAISecretLocator:
		// mcpServerConfigUpdateRequestModelRequestHeaders.ConvAISecretLocator is populated
	case components.MCPServerConfigUpdateRequestModelRequestHeadersTypeConvAIDynamicVariable:
		// mcpServerConfigUpdateRequestModelRequestHeaders.ConvAIDynamicVariable is populated
	case components.MCPServerConfigUpdateRequestModelRequestHeadersTypeConvAIEnvVarLocator:
		// mcpServerConfigUpdateRequestModelRequestHeaders.ConvAIEnvVarLocator is populated
}
```
