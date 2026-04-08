# GetToolCallUnitTestResponseModelDynamicVariables


## Supported Types

### 

```go
getToolCallUnitTestResponseModelDynamicVariables := components.CreateGetToolCallUnitTestResponseModelDynamicVariablesStr(string{/* values here */})
```

### 

```go
getToolCallUnitTestResponseModelDynamicVariables := components.CreateGetToolCallUnitTestResponseModelDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
getToolCallUnitTestResponseModelDynamicVariables := components.CreateGetToolCallUnitTestResponseModelDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
getToolCallUnitTestResponseModelDynamicVariables := components.CreateGetToolCallUnitTestResponseModelDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getToolCallUnitTestResponseModelDynamicVariables.Type {
	case components.GetToolCallUnitTestResponseModelDynamicVariablesTypeStr:
		// getToolCallUnitTestResponseModelDynamicVariables.Str is populated
	case components.GetToolCallUnitTestResponseModelDynamicVariablesTypeNumber:
		// getToolCallUnitTestResponseModelDynamicVariables.Number is populated
	case components.GetToolCallUnitTestResponseModelDynamicVariablesTypeInteger:
		// getToolCallUnitTestResponseModelDynamicVariables.Integer is populated
	case components.GetToolCallUnitTestResponseModelDynamicVariablesTypeBoolean:
		// getToolCallUnitTestResponseModelDynamicVariables.Boolean is populated
	default:
		// Unknown type - use getToolCallUnitTestResponseModelDynamicVariables.GetUnknownRaw() for raw JSON
}
```
