# MCPServerConfigInputRequestHeaders


## Supported Types

### 

```go
mcpServerConfigInputRequestHeaders := components.CreateMCPServerConfigInputRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
mcpServerConfigInputRequestHeaders := components.CreateMCPServerConfigInputRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
mcpServerConfigInputRequestHeaders := components.CreateMCPServerConfigInputRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

### ConvAIEnvVarLocator

```go
mcpServerConfigInputRequestHeaders := components.CreateMCPServerConfigInputRequestHeadersConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigInputRequestHeaders.Type {
	case components.MCPServerConfigInputRequestHeadersTypeStr:
		// mcpServerConfigInputRequestHeaders.Str is populated
	case components.MCPServerConfigInputRequestHeadersTypeConvAISecretLocator:
		// mcpServerConfigInputRequestHeaders.ConvAISecretLocator is populated
	case components.MCPServerConfigInputRequestHeadersTypeConvAIDynamicVariable:
		// mcpServerConfigInputRequestHeaders.ConvAIDynamicVariable is populated
	case components.MCPServerConfigInputRequestHeadersTypeConvAIEnvVarLocator:
		// mcpServerConfigInputRequestHeaders.ConvAIEnvVarLocator is populated
}
```
