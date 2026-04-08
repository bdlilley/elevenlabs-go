# WebhookToolAPISchemaConfigInputAuthConnection

Optional auth connection to use for authentication with this webhook


## Supported Types

### AuthConnectionLocator

```go
webhookToolAPISchemaConfigInputAuthConnection := components.CreateWebhookToolAPISchemaConfigInputAuthConnectionAuthConnectionLocator(components.AuthConnectionLocator{/* values here */})
```

### EnvironmentAuthConnectionLocator

```go
webhookToolAPISchemaConfigInputAuthConnection := components.CreateWebhookToolAPISchemaConfigInputAuthConnectionEnvironmentAuthConnectionLocator(components.EnvironmentAuthConnectionLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch webhookToolAPISchemaConfigInputAuthConnection.Type {
	case components.WebhookToolAPISchemaConfigInputAuthConnectionTypeAuthConnectionLocator:
		// webhookToolAPISchemaConfigInputAuthConnection.AuthConnectionLocator is populated
	case components.WebhookToolAPISchemaConfigInputAuthConnectionTypeEnvironmentAuthConnectionLocator:
		// webhookToolAPISchemaConfigInputAuthConnection.EnvironmentAuthConnectionLocator is populated
}
```
