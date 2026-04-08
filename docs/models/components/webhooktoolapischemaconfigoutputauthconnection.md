# WebhookToolAPISchemaConfigOutputAuthConnection

Optional auth connection to use for authentication with this webhook


## Supported Types

### AuthConnectionLocator

```go
webhookToolAPISchemaConfigOutputAuthConnection := components.CreateWebhookToolAPISchemaConfigOutputAuthConnectionAuthConnectionLocator(components.AuthConnectionLocator{/* values here */})
```

### EnvironmentAuthConnectionLocator

```go
webhookToolAPISchemaConfigOutputAuthConnection := components.CreateWebhookToolAPISchemaConfigOutputAuthConnectionEnvironmentAuthConnectionLocator(components.EnvironmentAuthConnectionLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch webhookToolAPISchemaConfigOutputAuthConnection.Type {
	case components.WebhookToolAPISchemaConfigOutputAuthConnectionTypeAuthConnectionLocator:
		// webhookToolAPISchemaConfigOutputAuthConnection.AuthConnectionLocator is populated
	case components.WebhookToolAPISchemaConfigOutputAuthConnectionTypeEnvironmentAuthConnectionLocator:
		// webhookToolAPISchemaConfigOutputAuthConnection.EnvironmentAuthConnectionLocator is populated
}
```
