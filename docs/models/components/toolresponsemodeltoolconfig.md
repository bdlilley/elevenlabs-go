# ToolResponseModelToolConfig

The type of tool


## Supported Types

### ClientToolConfigOutput

```go
toolResponseModelToolConfig := components.CreateToolResponseModelToolConfigClient(components.ClientToolConfigOutput{/* values here */})
```

### MCPToolConfigOutput

```go
toolResponseModelToolConfig := components.CreateToolResponseModelToolConfigMcp(components.MCPToolConfigOutput{/* values here */})
```

### SystemToolConfigOutput

```go
toolResponseModelToolConfig := components.CreateToolResponseModelToolConfigSystem(components.SystemToolConfigOutput{/* values here */})
```

### WebhookToolConfigOutput

```go
toolResponseModelToolConfig := components.CreateToolResponseModelToolConfigWebhook(components.WebhookToolConfigOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch toolResponseModelToolConfig.Type {
	case components.ToolResponseModelToolConfigTypeClient:
		// toolResponseModelToolConfig.ClientToolConfigOutput is populated
	case components.ToolResponseModelToolConfigTypeMcp:
		// toolResponseModelToolConfig.MCPToolConfigOutput is populated
	case components.ToolResponseModelToolConfigTypeSystem:
		// toolResponseModelToolConfig.SystemToolConfigOutput is populated
	case components.ToolResponseModelToolConfigTypeWebhook:
		// toolResponseModelToolConfig.WebhookToolConfigOutput is populated
	default:
		// Unknown type - use toolResponseModelToolConfig.GetUnknownRaw() for raw JSON
}
```
