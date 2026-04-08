# CreateToolCallUnitTestRequestDynamicVariables


## Supported Types

### 

```go
createToolCallUnitTestRequestDynamicVariables := components.CreateCreateToolCallUnitTestRequestDynamicVariablesStr(string{/* values here */})
```

### 

```go
createToolCallUnitTestRequestDynamicVariables := components.CreateCreateToolCallUnitTestRequestDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
createToolCallUnitTestRequestDynamicVariables := components.CreateCreateToolCallUnitTestRequestDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
createToolCallUnitTestRequestDynamicVariables := components.CreateCreateToolCallUnitTestRequestDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch createToolCallUnitTestRequestDynamicVariables.Type {
	case components.CreateToolCallUnitTestRequestDynamicVariablesTypeStr:
		// createToolCallUnitTestRequestDynamicVariables.Str is populated
	case components.CreateToolCallUnitTestRequestDynamicVariablesTypeNumber:
		// createToolCallUnitTestRequestDynamicVariables.Number is populated
	case components.CreateToolCallUnitTestRequestDynamicVariablesTypeInteger:
		// createToolCallUnitTestRequestDynamicVariables.Integer is populated
	case components.CreateToolCallUnitTestRequestDynamicVariablesTypeBoolean:
		// createToolCallUnitTestRequestDynamicVariables.Boolean is populated
}
```
