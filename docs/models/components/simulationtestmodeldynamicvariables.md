# SimulationTestModelDynamicVariables


## Supported Types

### 

```go
simulationTestModelDynamicVariables := components.CreateSimulationTestModelDynamicVariablesStr(string{/* values here */})
```

### 

```go
simulationTestModelDynamicVariables := components.CreateSimulationTestModelDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
simulationTestModelDynamicVariables := components.CreateSimulationTestModelDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
simulationTestModelDynamicVariables := components.CreateSimulationTestModelDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch simulationTestModelDynamicVariables.Type {
	case components.SimulationTestModelDynamicVariablesTypeStr:
		// simulationTestModelDynamicVariables.Str is populated
	case components.SimulationTestModelDynamicVariablesTypeNumber:
		// simulationTestModelDynamicVariables.Number is populated
	case components.SimulationTestModelDynamicVariablesTypeInteger:
		// simulationTestModelDynamicVariables.Integer is populated
	case components.SimulationTestModelDynamicVariablesTypeBoolean:
		// simulationTestModelDynamicVariables.Boolean is populated
	default:
		// Unknown type - use simulationTestModelDynamicVariables.GetUnknownRaw() for raw JSON
}
```
