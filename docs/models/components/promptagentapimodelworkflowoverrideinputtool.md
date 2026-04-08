# PromptAgentAPIModelWorkflowOverrideInputTool

The type of tool


## Supported Types

### APIIntegrationWebhookToolConfigInput

```go
promptAgentAPIModelWorkflowOverrideInputTool := components.CreatePromptAgentAPIModelWorkflowOverrideInputToolAPIIntegrationWebhook(components.APIIntegrationWebhookToolConfigInput{/* values here */})
```

### ClientToolConfigInput

```go
promptAgentAPIModelWorkflowOverrideInputTool := components.CreatePromptAgentAPIModelWorkflowOverrideInputToolClient(components.ClientToolConfigInput{/* values here */})
```

### MCPToolConfigInput

```go
promptAgentAPIModelWorkflowOverrideInputTool := components.CreatePromptAgentAPIModelWorkflowOverrideInputToolMcp(components.MCPToolConfigInput{/* values here */})
```

### SMBToolConfig

```go
promptAgentAPIModelWorkflowOverrideInputTool := components.CreatePromptAgentAPIModelWorkflowOverrideInputToolSmb(components.SMBToolConfig{/* values here */})
```

### SystemToolConfigInput

```go
promptAgentAPIModelWorkflowOverrideInputTool := components.CreatePromptAgentAPIModelWorkflowOverrideInputToolSystem(components.SystemToolConfigInput{/* values here */})
```

### WebhookToolConfigInput

```go
promptAgentAPIModelWorkflowOverrideInputTool := components.CreatePromptAgentAPIModelWorkflowOverrideInputToolWebhook(components.WebhookToolConfigInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelWorkflowOverrideInputTool.Type {
	case components.PromptAgentAPIModelWorkflowOverrideInputToolTypeAPIIntegrationWebhook:
		// promptAgentAPIModelWorkflowOverrideInputTool.APIIntegrationWebhookToolConfigInput is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputToolTypeClient:
		// promptAgentAPIModelWorkflowOverrideInputTool.ClientToolConfigInput is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputToolTypeMcp:
		// promptAgentAPIModelWorkflowOverrideInputTool.MCPToolConfigInput is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputToolTypeSmb:
		// promptAgentAPIModelWorkflowOverrideInputTool.SMBToolConfig is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputToolTypeSystem:
		// promptAgentAPIModelWorkflowOverrideInputTool.SystemToolConfigInput is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputToolTypeWebhook:
		// promptAgentAPIModelWorkflowOverrideInputTool.WebhookToolConfigInput is populated
}
```
