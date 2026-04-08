# MCPServerConfigOutputRequestHeaders


## Supported Types

### 

```go
mcpServerConfigOutputRequestHeaders := components.CreateMCPServerConfigOutputRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
mcpServerConfigOutputRequestHeaders := components.CreateMCPServerConfigOutputRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
mcpServerConfigOutputRequestHeaders := components.CreateMCPServerConfigOutputRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

### ConvAIEnvVarLocator

```go
mcpServerConfigOutputRequestHeaders := components.CreateMCPServerConfigOutputRequestHeadersConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigOutputRequestHeaders.Type {
	case components.MCPServerConfigOutputRequestHeadersTypeStr:
		// mcpServerConfigOutputRequestHeaders.Str is populated
	case components.MCPServerConfigOutputRequestHeadersTypeConvAISecretLocator:
		// mcpServerConfigOutputRequestHeaders.ConvAISecretLocator is populated
	case components.MCPServerConfigOutputRequestHeadersTypeConvAIDynamicVariable:
		// mcpServerConfigOutputRequestHeaders.ConvAIDynamicVariable is populated
	case components.MCPServerConfigOutputRequestHeadersTypeConvAIEnvVarLocator:
		// mcpServerConfigOutputRequestHeaders.ConvAIEnvVarLocator is populated
	default:
		// Unknown type - use mcpServerConfigOutputRequestHeaders.GetUnknownRaw() for raw JSON
}
```
