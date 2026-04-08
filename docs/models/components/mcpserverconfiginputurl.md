# MCPServerConfigInputURL

The URL of the MCP server, if this contains a secret please store as a workspace secret, otherwise store as a plain string. Must use https


## Supported Types

### 

```go
mcpServerConfigInputURL := components.CreateMCPServerConfigInputURLStr(string{/* values here */})
```

### ConvAISecretLocator

```go
mcpServerConfigInputURL := components.CreateMCPServerConfigInputURLConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigInputURL.Type {
	case components.MCPServerConfigInputURLTypeStr:
		// mcpServerConfigInputURL.Str is populated
	case components.MCPServerConfigInputURLTypeConvAISecretLocator:
		// mcpServerConfigInputURL.ConvAISecretLocator is populated
}
```
