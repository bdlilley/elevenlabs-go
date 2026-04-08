# WebhookToolAPISchemaConfigInputRequestHeaders


## Supported Types

### 

```go
webhookToolAPISchemaConfigInputRequestHeaders := components.CreateWebhookToolAPISchemaConfigInputRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
webhookToolAPISchemaConfigInputRequestHeaders := components.CreateWebhookToolAPISchemaConfigInputRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
webhookToolAPISchemaConfigInputRequestHeaders := components.CreateWebhookToolAPISchemaConfigInputRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

### ConvAIEnvVarLocator

```go
webhookToolAPISchemaConfigInputRequestHeaders := components.CreateWebhookToolAPISchemaConfigInputRequestHeadersConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch webhookToolAPISchemaConfigInputRequestHeaders.Type {
	case components.WebhookToolAPISchemaConfigInputRequestHeadersTypeStr:
		// webhookToolAPISchemaConfigInputRequestHeaders.Str is populated
	case components.WebhookToolAPISchemaConfigInputRequestHeadersTypeConvAISecretLocator:
		// webhookToolAPISchemaConfigInputRequestHeaders.ConvAISecretLocator is populated
	case components.WebhookToolAPISchemaConfigInputRequestHeadersTypeConvAIDynamicVariable:
		// webhookToolAPISchemaConfigInputRequestHeaders.ConvAIDynamicVariable is populated
	case components.WebhookToolAPISchemaConfigInputRequestHeadersTypeConvAIEnvVarLocator:
		// webhookToolAPISchemaConfigInputRequestHeaders.ConvAIEnvVarLocator is populated
}
```
