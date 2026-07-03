# CustomLLMAuthConnection

Optional workspace auth connection for authentication. Only auth connections that produce an Authorization Bearer token are supported; Basic auth, mTLS, custom header, and URL secret auth connections are not supported.


## Supported Types

### AuthConnectionLocator

```go
customLLMAuthConnection := components.CreateCustomLLMAuthConnectionAuthConnectionLocator(components.AuthConnectionLocator{/* values here */})
```

### EnvironmentAuthConnectionLocator

```go
customLLMAuthConnection := components.CreateCustomLLMAuthConnectionEnvironmentAuthConnectionLocator(components.EnvironmentAuthConnectionLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch customLLMAuthConnection.Type {
	case components.CustomLLMAuthConnectionTypeAuthConnectionLocator:
		// customLLMAuthConnection.AuthConnectionLocator is populated
	case components.CustomLLMAuthConnectionTypeEnvironmentAuthConnectionLocator:
		// customLLMAuthConnection.EnvironmentAuthConnectionLocator is populated
}
```
