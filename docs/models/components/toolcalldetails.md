# ToolCallDetails


## Supported Types

### ConversationHistoryTranscriptToolCallAPIIntegrationWebhookDetailsOutput

```go
toolCallDetails := components.CreateToolCallDetailsAPIIntegrationWebhook(components.ConversationHistoryTranscriptToolCallAPIIntegrationWebhookDetailsOutput{/* values here */})
```

### ConversationHistoryTranscriptToolCallClientDetails

```go
toolCallDetails := components.CreateToolCallDetailsClient(components.ConversationHistoryTranscriptToolCallClientDetails{/* values here */})
```

### ConversationHistoryTranscriptToolCallMCPDetails

```go
toolCallDetails := components.CreateToolCallDetailsMcp(components.ConversationHistoryTranscriptToolCallMCPDetails{/* values here */})
```

### ConversationHistoryTranscriptToolCallWebhookDetails

```go
toolCallDetails := components.CreateToolCallDetailsWebhook(components.ConversationHistoryTranscriptToolCallWebhookDetails{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch toolCallDetails.Type {
	case components.ToolCallDetailsTypeAPIIntegrationWebhook:
		// toolCallDetails.ConversationHistoryTranscriptToolCallAPIIntegrationWebhookDetailsOutput is populated
	case components.ToolCallDetailsTypeClient:
		// toolCallDetails.ConversationHistoryTranscriptToolCallClientDetails is populated
	case components.ToolCallDetailsTypeMcp:
		// toolCallDetails.ConversationHistoryTranscriptToolCallMCPDetails is populated
	case components.ToolCallDetailsTypeWebhook:
		// toolCallDetails.ConversationHistoryTranscriptToolCallWebhookDetails is populated
}
```
