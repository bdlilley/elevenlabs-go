# AgentsPlatformCreateEnvironmentVariableRequest


## Supported Types

### CreateStringEnvironmentVariableRequest

```go
agentsPlatformCreateEnvironmentVariableRequest := operations.CreateAgentsPlatformCreateEnvironmentVariableRequestString(components.CreateStringEnvironmentVariableRequest{/* values here */})
```

### CreateSecretEnvironmentVariableRequest

```go
agentsPlatformCreateEnvironmentVariableRequest := operations.CreateAgentsPlatformCreateEnvironmentVariableRequestSecret(components.CreateSecretEnvironmentVariableRequest{/* values here */})
```

### CreateAuthConnectionEnvironmentVariableRequest

```go
agentsPlatformCreateEnvironmentVariableRequest := operations.CreateAgentsPlatformCreateEnvironmentVariableRequestAuthConnection(components.CreateAuthConnectionEnvironmentVariableRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch agentsPlatformCreateEnvironmentVariableRequest.Type {
	case operations.AgentsPlatformCreateEnvironmentVariableRequestTypeString:
		// agentsPlatformCreateEnvironmentVariableRequest.CreateStringEnvironmentVariableRequest is populated
	case operations.AgentsPlatformCreateEnvironmentVariableRequestTypeSecret:
		// agentsPlatformCreateEnvironmentVariableRequest.CreateSecretEnvironmentVariableRequest is populated
	case operations.AgentsPlatformCreateEnvironmentVariableRequestTypeAuthConnection:
		// agentsPlatformCreateEnvironmentVariableRequest.CreateAuthConnectionEnvironmentVariableRequest is populated
}
```
