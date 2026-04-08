# CreateSimulationTestRequestDynamicVariables


## Supported Types

### 

```go
createSimulationTestRequestDynamicVariables := components.CreateCreateSimulationTestRequestDynamicVariablesStr(string{/* values here */})
```

### 

```go
createSimulationTestRequestDynamicVariables := components.CreateCreateSimulationTestRequestDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
createSimulationTestRequestDynamicVariables := components.CreateCreateSimulationTestRequestDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
createSimulationTestRequestDynamicVariables := components.CreateCreateSimulationTestRequestDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch createSimulationTestRequestDynamicVariables.Type {
	case components.CreateSimulationTestRequestDynamicVariablesTypeStr:
		// createSimulationTestRequestDynamicVariables.Str is populated
	case components.CreateSimulationTestRequestDynamicVariablesTypeNumber:
		// createSimulationTestRequestDynamicVariables.Number is populated
	case components.CreateSimulationTestRequestDynamicVariablesTypeInteger:
		// createSimulationTestRequestDynamicVariables.Integer is populated
	case components.CreateSimulationTestRequestDynamicVariablesTypeBoolean:
		// createSimulationTestRequestDynamicVariables.Boolean is populated
}
```
