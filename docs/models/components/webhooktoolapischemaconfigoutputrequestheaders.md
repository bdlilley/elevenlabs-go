# WebhookToolAPISchemaConfigOutputRequestHeaders


## Supported Types

### 

```go
webhookToolAPISchemaConfigOutputRequestHeaders := components.CreateWebhookToolAPISchemaConfigOutputRequestHeadersStr(string{/* values here */})
```

### ConvAISecretLocator

```go
webhookToolAPISchemaConfigOutputRequestHeaders := components.CreateWebhookToolAPISchemaConfigOutputRequestHeadersConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIDynamicVariable

```go
webhookToolAPISchemaConfigOutputRequestHeaders := components.CreateWebhookToolAPISchemaConfigOutputRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

### ConvAIEnvVarLocator

```go
webhookToolAPISchemaConfigOutputRequestHeaders := components.CreateWebhookToolAPISchemaConfigOutputRequestHeadersConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch webhookToolAPISchemaConfigOutputRequestHeaders.Type {
	case components.WebhookToolAPISchemaConfigOutputRequestHeadersTypeStr:
		// webhookToolAPISchemaConfigOutputRequestHeaders.Str is populated
	case components.WebhookToolAPISchemaConfigOutputRequestHeadersTypeConvAISecretLocator:
		// webhookToolAPISchemaConfigOutputRequestHeaders.ConvAISecretLocator is populated
	case components.WebhookToolAPISchemaConfigOutputRequestHeadersTypeConvAIDynamicVariable:
		// webhookToolAPISchemaConfigOutputRequestHeaders.ConvAIDynamicVariable is populated
	case components.WebhookToolAPISchemaConfigOutputRequestHeadersTypeConvAIEnvVarLocator:
		// webhookToolAPISchemaConfigOutputRequestHeaders.ConvAIEnvVarLocator is populated
}
```
