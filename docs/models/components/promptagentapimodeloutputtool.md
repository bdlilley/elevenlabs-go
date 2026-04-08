# PromptAgentAPIModelOutputTool

The type of tool


## Supported Types

### APIIntegrationWebhookToolConfigOutput

```go
promptAgentAPIModelOutputTool := components.CreatePromptAgentAPIModelOutputToolAPIIntegrationWebhook(components.APIIntegrationWebhookToolConfigOutput{/* values here */})
```

### ClientToolConfigOutput

```go
promptAgentAPIModelOutputTool := components.CreatePromptAgentAPIModelOutputToolClient(components.ClientToolConfigOutput{/* values here */})
```

### MCPToolConfigOutput

```go
promptAgentAPIModelOutputTool := components.CreatePromptAgentAPIModelOutputToolMcp(components.MCPToolConfigOutput{/* values here */})
```

### SMBToolConfig

```go
promptAgentAPIModelOutputTool := components.CreatePromptAgentAPIModelOutputToolSmb(components.SMBToolConfig{/* values here */})
```

### SystemToolConfigOutput

```go
promptAgentAPIModelOutputTool := components.CreatePromptAgentAPIModelOutputToolSystem(components.SystemToolConfigOutput{/* values here */})
```

### WebhookToolConfigOutput

```go
promptAgentAPIModelOutputTool := components.CreatePromptAgentAPIModelOutputToolWebhook(components.WebhookToolConfigOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelOutputTool.Type {
	case components.PromptAgentAPIModelOutputToolTypeAPIIntegrationWebhook:
		// promptAgentAPIModelOutputTool.APIIntegrationWebhookToolConfigOutput is populated
	case components.PromptAgentAPIModelOutputToolTypeClient:
		// promptAgentAPIModelOutputTool.ClientToolConfigOutput is populated
	case components.PromptAgentAPIModelOutputToolTypeMcp:
		// promptAgentAPIModelOutputTool.MCPToolConfigOutput is populated
	case components.PromptAgentAPIModelOutputToolTypeSmb:
		// promptAgentAPIModelOutputTool.SMBToolConfig is populated
	case components.PromptAgentAPIModelOutputToolTypeSystem:
		// promptAgentAPIModelOutputTool.SystemToolConfigOutput is populated
	case components.PromptAgentAPIModelOutputToolTypeWebhook:
		// promptAgentAPIModelOutputTool.WebhookToolConfigOutput is populated
}
```
