# ToolCallUnitTestModelDynamicVariables


## Supported Types

### 

```go
toolCallUnitTestModelDynamicVariables := components.CreateToolCallUnitTestModelDynamicVariablesStr(string{/* values here */})
```

### 

```go
toolCallUnitTestModelDynamicVariables := components.CreateToolCallUnitTestModelDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
toolCallUnitTestModelDynamicVariables := components.CreateToolCallUnitTestModelDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
toolCallUnitTestModelDynamicVariables := components.CreateToolCallUnitTestModelDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch toolCallUnitTestModelDynamicVariables.Type {
	case components.ToolCallUnitTestModelDynamicVariablesTypeStr:
		// toolCallUnitTestModelDynamicVariables.Str is populated
	case components.ToolCallUnitTestModelDynamicVariablesTypeNumber:
		// toolCallUnitTestModelDynamicVariables.Number is populated
	case components.ToolCallUnitTestModelDynamicVariablesTypeInteger:
		// toolCallUnitTestModelDynamicVariables.Integer is populated
	case components.ToolCallUnitTestModelDynamicVariablesTypeBoolean:
		// toolCallUnitTestModelDynamicVariables.Boolean is populated
	default:
		// Unknown type - use toolCallUnitTestModelDynamicVariables.GetUnknownRaw() for raw JSON
}
```
