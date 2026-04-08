# EnvironmentVariableResponseValues


## Supported Types

### 

```go
environmentVariableResponseValues := components.CreateEnvironmentVariableResponseValuesMapOfStr(map[string]string{/* values here */})
```

### 

```go
environmentVariableResponseValues := components.CreateEnvironmentVariableResponseValuesMapOfEnvironmentVariableSecretValue(map[string]components.EnvironmentVariableSecretValue{/* values here */})
```

### 

```go
environmentVariableResponseValues := components.CreateEnvironmentVariableResponseValuesMapOfEnvironmentVariableAuthConnectionValue(map[string]components.EnvironmentVariableAuthConnectionValue{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch environmentVariableResponseValues.Type {
	case components.EnvironmentVariableResponseValuesTypeMapOfStr:
		// environmentVariableResponseValues.MapOfStr is populated
	case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableSecretValue:
		// environmentVariableResponseValues.MapOfEnvironmentVariableSecretValue is populated
	case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableAuthConnectionValue:
		// environmentVariableResponseValues.MapOfEnvironmentVariableAuthConnectionValue is populated
}
```
