# GetSimulationTestResponseModelDynamicVariables


## Supported Types

### 

```go
getSimulationTestResponseModelDynamicVariables := components.CreateGetSimulationTestResponseModelDynamicVariablesStr(string{/* values here */})
```

### 

```go
getSimulationTestResponseModelDynamicVariables := components.CreateGetSimulationTestResponseModelDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
getSimulationTestResponseModelDynamicVariables := components.CreateGetSimulationTestResponseModelDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
getSimulationTestResponseModelDynamicVariables := components.CreateGetSimulationTestResponseModelDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getSimulationTestResponseModelDynamicVariables.Type {
	case components.GetSimulationTestResponseModelDynamicVariablesTypeStr:
		// getSimulationTestResponseModelDynamicVariables.Str is populated
	case components.GetSimulationTestResponseModelDynamicVariablesTypeNumber:
		// getSimulationTestResponseModelDynamicVariables.Number is populated
	case components.GetSimulationTestResponseModelDynamicVariablesTypeInteger:
		// getSimulationTestResponseModelDynamicVariables.Integer is populated
	case components.GetSimulationTestResponseModelDynamicVariablesTypeBoolean:
		// getSimulationTestResponseModelDynamicVariables.Boolean is populated
}
```
