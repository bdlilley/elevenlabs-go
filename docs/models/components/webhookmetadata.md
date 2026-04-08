# WebhookMetadata

Optional metadata to be included in the webhook response. This should be a JSON string representing an object with a maximum depth of 2 levels and maximum size of 16KB. Useful for tracking internal IDs, job references, or other contextual information.


## Supported Types

### 

```go
webhookMetadata := components.CreateWebhookMetadataStr(string{/* values here */})
```

### 

```go
webhookMetadata := components.CreateWebhookMetadataMapOfAny(map[string]any{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch webhookMetadata.Type {
	case components.WebhookMetadataTypeStr:
		// webhookMetadata.Str is populated
	case components.WebhookMetadataTypeMapOfAny:
		// webhookMetadata.MapOfAny is populated
}
```
