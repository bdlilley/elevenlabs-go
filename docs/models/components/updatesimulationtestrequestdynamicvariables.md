# UpdateSimulationTestRequestDynamicVariables


## Supported Types

### 

```go
updateSimulationTestRequestDynamicVariables := components.CreateUpdateSimulationTestRequestDynamicVariablesStr(string{/* values here */})
```

### 

```go
updateSimulationTestRequestDynamicVariables := components.CreateUpdateSimulationTestRequestDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
updateSimulationTestRequestDynamicVariables := components.CreateUpdateSimulationTestRequestDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
updateSimulationTestRequestDynamicVariables := components.CreateUpdateSimulationTestRequestDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch updateSimulationTestRequestDynamicVariables.Type {
	case components.UpdateSimulationTestRequestDynamicVariablesTypeStr:
		// updateSimulationTestRequestDynamicVariables.Str is populated
	case components.UpdateSimulationTestRequestDynamicVariablesTypeNumber:
		// updateSimulationTestRequestDynamicVariables.Number is populated
	case components.UpdateSimulationTestRequestDynamicVariablesTypeInteger:
		// updateSimulationTestRequestDynamicVariables.Integer is populated
	case components.UpdateSimulationTestRequestDynamicVariablesTypeBoolean:
		// updateSimulationTestRequestDynamicVariables.Boolean is populated
}
```
