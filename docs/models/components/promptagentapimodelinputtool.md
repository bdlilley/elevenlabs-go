# PromptAgentAPIModelInputTool

The type of tool


## Supported Types

### APIIntegrationWebhookToolConfigInput

```go
promptAgentAPIModelInputTool := components.CreatePromptAgentAPIModelInputToolAPIIntegrationWebhook(components.APIIntegrationWebhookToolConfigInput{/* values here */})
```

### ClientToolConfigInput

```go
promptAgentAPIModelInputTool := components.CreatePromptAgentAPIModelInputToolClient(components.ClientToolConfigInput{/* values here */})
```

### MCPToolConfigInput

```go
promptAgentAPIModelInputTool := components.CreatePromptAgentAPIModelInputToolMcp(components.MCPToolConfigInput{/* values here */})
```

### SMBToolConfig

```go
promptAgentAPIModelInputTool := components.CreatePromptAgentAPIModelInputToolSmb(components.SMBToolConfig{/* values here */})
```

### SystemToolConfigInput

```go
promptAgentAPIModelInputTool := components.CreatePromptAgentAPIModelInputToolSystem(components.SystemToolConfigInput{/* values here */})
```

### WebhookToolConfigInput

```go
promptAgentAPIModelInputTool := components.CreatePromptAgentAPIModelInputToolWebhook(components.WebhookToolConfigInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelInputTool.Type {
	case components.PromptAgentAPIModelInputToolTypeAPIIntegrationWebhook:
		// promptAgentAPIModelInputTool.APIIntegrationWebhookToolConfigInput is populated
	case components.PromptAgentAPIModelInputToolTypeClient:
		// promptAgentAPIModelInputTool.ClientToolConfigInput is populated
	case components.PromptAgentAPIModelInputToolTypeMcp:
		// promptAgentAPIModelInputTool.MCPToolConfigInput is populated
	case components.PromptAgentAPIModelInputToolTypeSmb:
		// promptAgentAPIModelInputTool.SMBToolConfig is populated
	case components.PromptAgentAPIModelInputToolTypeSystem:
		// promptAgentAPIModelInputTool.SystemToolConfigInput is populated
	case components.PromptAgentAPIModelInputToolTypeWebhook:
		// promptAgentAPIModelInputTool.WebhookToolConfigInput is populated
}
```
