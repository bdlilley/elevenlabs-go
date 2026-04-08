# MCPServerConfigOutputSecretToken

The secret token (Authorization header) stored as a workspace secret or in-place secret


## Supported Types

### ConvAISecretLocator

```go
mcpServerConfigOutputSecretToken := components.CreateMCPServerConfigOutputSecretTokenConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIUserSecretDBModel

```go
mcpServerConfigOutputSecretToken := components.CreateMCPServerConfigOutputSecretTokenConvAIUserSecretDBModel(components.ConvAIUserSecretDBModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigOutputSecretToken.Type {
	case components.MCPServerConfigOutputSecretTokenTypeConvAISecretLocator:
		// mcpServerConfigOutputSecretToken.ConvAISecretLocator is populated
	case components.MCPServerConfigOutputSecretTokenTypeConvAIUserSecretDBModel:
		// mcpServerConfigOutputSecretToken.ConvAIUserSecretDBModel is populated
}
```
