# MCPServerConfigOutputURL

The URL of the MCP server, if this contains a secret please store as a workspace secret, otherwise store as a plain string. Must use https


## Supported Types

### 

```go
mcpServerConfigOutputURL := components.CreateMCPServerConfigOutputURLStr(string{/* values here */})
```

### ConvAISecretLocator

```go
mcpServerConfigOutputURL := components.CreateMCPServerConfigOutputURLConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigOutputURL.Type {
	case components.MCPServerConfigOutputURLTypeStr:
		// mcpServerConfigOutputURL.Str is populated
	case components.MCPServerConfigOutputURLTypeConvAISecretLocator:
		// mcpServerConfigOutputURL.ConvAISecretLocator is populated
	default:
		// Unknown type - use mcpServerConfigOutputURL.GetUnknownRaw() for raw JSON
}
```
