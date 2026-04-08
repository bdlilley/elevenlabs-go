# UpdateToolCallUnitTestRequestDynamicVariables


## Supported Types

### 

```go
updateToolCallUnitTestRequestDynamicVariables := components.CreateUpdateToolCallUnitTestRequestDynamicVariablesStr(string{/* values here */})
```

### 

```go
updateToolCallUnitTestRequestDynamicVariables := components.CreateUpdateToolCallUnitTestRequestDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
updateToolCallUnitTestRequestDynamicVariables := components.CreateUpdateToolCallUnitTestRequestDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
updateToolCallUnitTestRequestDynamicVariables := components.CreateUpdateToolCallUnitTestRequestDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch updateToolCallUnitTestRequestDynamicVariables.Type {
	case components.UpdateToolCallUnitTestRequestDynamicVariablesTypeStr:
		// updateToolCallUnitTestRequestDynamicVariables.Str is populated
	case components.UpdateToolCallUnitTestRequestDynamicVariablesTypeNumber:
		// updateToolCallUnitTestRequestDynamicVariables.Number is populated
	case components.UpdateToolCallUnitTestRequestDynamicVariablesTypeInteger:
		// updateToolCallUnitTestRequestDynamicVariables.Integer is populated
	case components.UpdateToolCallUnitTestRequestDynamicVariablesTypeBoolean:
		// updateToolCallUnitTestRequestDynamicVariables.Boolean is populated
}
```
