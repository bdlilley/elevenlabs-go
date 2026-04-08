# PromptAgentAPIModelWorkflowOverrideOutputTool

The type of tool


## Supported Types

### APIIntegrationWebhookToolConfigOutput

```go
promptAgentAPIModelWorkflowOverrideOutputTool := components.CreatePromptAgentAPIModelWorkflowOverrideOutputToolAPIIntegrationWebhook(components.APIIntegrationWebhookToolConfigOutput{/* values here */})
```

### ClientToolConfigOutput

```go
promptAgentAPIModelWorkflowOverrideOutputTool := components.CreatePromptAgentAPIModelWorkflowOverrideOutputToolClient(components.ClientToolConfigOutput{/* values here */})
```

### MCPToolConfigOutput

```go
promptAgentAPIModelWorkflowOverrideOutputTool := components.CreatePromptAgentAPIModelWorkflowOverrideOutputToolMcp(components.MCPToolConfigOutput{/* values here */})
```

### SMBToolConfig

```go
promptAgentAPIModelWorkflowOverrideOutputTool := components.CreatePromptAgentAPIModelWorkflowOverrideOutputToolSmb(components.SMBToolConfig{/* values here */})
```

### SystemToolConfigOutput

```go
promptAgentAPIModelWorkflowOverrideOutputTool := components.CreatePromptAgentAPIModelWorkflowOverrideOutputToolSystem(components.SystemToolConfigOutput{/* values here */})
```

### WebhookToolConfigOutput

```go
promptAgentAPIModelWorkflowOverrideOutputTool := components.CreatePromptAgentAPIModelWorkflowOverrideOutputToolWebhook(components.WebhookToolConfigOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelWorkflowOverrideOutputTool.Type {
	case components.PromptAgentAPIModelWorkflowOverrideOutputToolTypeAPIIntegrationWebhook:
		// promptAgentAPIModelWorkflowOverrideOutputTool.APIIntegrationWebhookToolConfigOutput is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputToolTypeClient:
		// promptAgentAPIModelWorkflowOverrideOutputTool.ClientToolConfigOutput is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputToolTypeMcp:
		// promptAgentAPIModelWorkflowOverrideOutputTool.MCPToolConfigOutput is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputToolTypeSmb:
		// promptAgentAPIModelWorkflowOverrideOutputTool.SMBToolConfig is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputToolTypeSystem:
		// promptAgentAPIModelWorkflowOverrideOutputTool.SystemToolConfigOutput is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputToolTypeWebhook:
		// promptAgentAPIModelWorkflowOverrideOutputTool.WebhookToolConfigOutput is populated
	default:
		// Unknown type - use promptAgentAPIModelWorkflowOverrideOutputTool.GetUnknownRaw() for raw JSON
}
```
