# CreateEnvironmentVariableRequest


## Supported Types

### CreateStringEnvironmentVariableRequest

```go
createEnvironmentVariableRequest := operations.CreateCreateEnvironmentVariableRequestString(components.CreateStringEnvironmentVariableRequest{/* values here */})
```

### CreateSecretEnvironmentVariableRequest

```go
createEnvironmentVariableRequest := operations.CreateCreateEnvironmentVariableRequestSecret(components.CreateSecretEnvironmentVariableRequest{/* values here */})
```

### CreateAuthConnectionEnvironmentVariableRequest

```go
createEnvironmentVariableRequest := operations.CreateCreateEnvironmentVariableRequestAuthConnection(components.CreateAuthConnectionEnvironmentVariableRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch createEnvironmentVariableRequest.Type {
	case operations.CreateEnvironmentVariableRequestTypeString:
		// createEnvironmentVariableRequest.CreateStringEnvironmentVariableRequest is populated
	case operations.CreateEnvironmentVariableRequestTypeSecret:
		// createEnvironmentVariableRequest.CreateSecretEnvironmentVariableRequest is populated
	case operations.CreateEnvironmentVariableRequestTypeAuthConnection:
		// createEnvironmentVariableRequest.CreateAuthConnectionEnvironmentVariableRequest is populated
}
```
