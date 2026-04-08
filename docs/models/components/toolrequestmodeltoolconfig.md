# ToolRequestModelToolConfig

Configuration for the tool


## Supported Types

### ClientToolConfigInput

```go
toolRequestModelToolConfig := components.CreateToolRequestModelToolConfigClient(components.ClientToolConfigInput{/* values here */})
```

### MCPToolConfigInput

```go
toolRequestModelToolConfig := components.CreateToolRequestModelToolConfigMcp(components.MCPToolConfigInput{/* values here */})
```

### SystemToolConfigInput

```go
toolRequestModelToolConfig := components.CreateToolRequestModelToolConfigSystem(components.SystemToolConfigInput{/* values here */})
```

### WebhookToolConfigInput

```go
toolRequestModelToolConfig := components.CreateToolRequestModelToolConfigWebhook(components.WebhookToolConfigInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch toolRequestModelToolConfig.Type {
	case components.ToolRequestModelToolConfigTypeClient:
		// toolRequestModelToolConfig.ClientToolConfigInput is populated
	case components.ToolRequestModelToolConfigTypeMcp:
		// toolRequestModelToolConfig.MCPToolConfigInput is populated
	case components.ToolRequestModelToolConfigTypeSystem:
		// toolRequestModelToolConfig.SystemToolConfigInput is populated
	case components.ToolRequestModelToolConfigTypeWebhook:
		// toolRequestModelToolConfig.WebhookToolConfigInput is populated
}
```
