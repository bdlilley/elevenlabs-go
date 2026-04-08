# APIKey

The API key for authentication. Either a workspace secret reference {'secret_id': '...'} or an environment variable reference {'env_var_label': '...'}.


## Supported Types

### ConvAISecretLocator

```go
apiKey := components.CreateAPIKeyConvAISecretLocator(components.ConvAISecretLocator{/* values here */})
```

### ConvAIEnvVarLocator

```go
apiKey := components.CreateAPIKeyConvAIEnvVarLocator(components.ConvAIEnvVarLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch apiKey.Type {
	case components.APIKeyTypeConvAISecretLocator:
		// apiKey.ConvAISecretLocator is populated
	case components.APIKeyTypeConvAIEnvVarLocator:
		// apiKey.ConvAIEnvVarLocator is populated
	default:
		// Unknown type - use apiKey.GetUnknownRaw() for raw JSON
}
```
