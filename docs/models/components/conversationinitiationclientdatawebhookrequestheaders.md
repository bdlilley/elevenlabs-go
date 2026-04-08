# ConversationInitiationClientDataWebhookRequestHeaders


## Supported Types

### 

```go
conversationInitiationClientDataWebhookRequestHeaders := components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
conversationInitiationClientDataWebhookRequestHeaders := components.CreateConversationInitiationClientDataWebhookRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch conversationInitiationClientDataWebhookRequestHeaders.Type {
	case components.ConversationInitiationClientDataWebhookRequestHeadersTypeStr:
		// conversationInitiationClientDataWebhookRequestHeaders.Str is populated
	case components.ConversationInitiationClientDataWebhookRequestHeadersTypeConvAISecretLocator:
		// conversationInitiationClientDataWebhookRequestHeaders.ConvAISecretLocator is populated
	default:
		// Unknown type - use conversationInitiationClientDataWebhookRequestHeaders.GetUnknownRaw() for raw JSON
}
```
