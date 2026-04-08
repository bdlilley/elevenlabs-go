# MCPServerConfigInputSecretToken

The secret token (Authorization header) stored as a workspace secret or in-place secret


## Supported Types

### ConvAISecretLocator

```go
mcpServerConfigInputSecretToken := components.CreateMCPServerConfigInputSecretTokenConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIUserSecretDBModel

```go
mcpServerConfigInputSecretToken := components.CreateMCPServerConfigInputSecretTokenConvAIUserSecretDBModel(components.ConvAIUserSecretDBModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigInputSecretToken.Type {
	case components.MCPServerConfigInputSecretTokenTypeConvAISecretLocator:
		// mcpServerConfigInputSecretToken.ConvAISecretLocator is populated
	case components.MCPServerConfigInputSecretTokenTypeConvAIUserSecretDBModel:
		// mcpServerConfigInputSecretToken.ConvAIUserSecretDBModel is populated
}
```
