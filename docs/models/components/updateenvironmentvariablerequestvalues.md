# UpdateEnvironmentVariableRequestValues


## Supported Types

### 

```go
updateEnvironmentVariableRequestValues := components.CreateUpdateEnvironmentVariableRequestValuesStr(string{/* values here */})
```

### EnvironmentVariableSecretValueRequest

```go
updateEnvironmentVariableRequestValues := components.CreateUpdateEnvironmentVariableRequestValuesEnvironmentVariableSecretValueRequest(components.EnvironmentVariableSecretValueRequest{/* values here */})
```

### EnvironmentVariableAuthConnectionValueRequest

```go
updateEnvironmentVariableRequestValues := components.CreateUpdateEnvironmentVariableRequestValuesEnvironmentVariableAuthConnectionValueRequest(components.EnvironmentVariableAuthConnectionValueRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch updateEnvironmentVariableRequestValues.Type {
	case components.UpdateEnvironmentVariableRequestValuesTypeStr:
		// updateEnvironmentVariableRequestValues.Str is populated
	case components.UpdateEnvironmentVariableRequestValuesTypeEnvironmentVariableSecretValueRequest:
		// updateEnvironmentVariableRequestValues.EnvironmentVariableSecretValueRequest is populated
	case components.UpdateEnvironmentVariableRequestValuesTypeEnvironmentVariableAuthConnectionValueRequest:
		// updateEnvironmentVariableRequestValues.EnvironmentVariableAuthConnectionValueRequest is populated
}
```
