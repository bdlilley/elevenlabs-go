# CreateResponseUnitTestRequestDynamicVariables


## Supported Types

### 

```go
createResponseUnitTestRequestDynamicVariables := components.CreateCreateResponseUnitTestRequestDynamicVariablesStr(string{/* values here */})
```

### 

```go
createResponseUnitTestRequestDynamicVariables := components.CreateCreateResponseUnitTestRequestDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
createResponseUnitTestRequestDynamicVariables := components.CreateCreateResponseUnitTestRequestDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
createResponseUnitTestRequestDynamicVariables := components.CreateCreateResponseUnitTestRequestDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch createResponseUnitTestRequestDynamicVariables.Type {
	case components.CreateResponseUnitTestRequestDynamicVariablesTypeStr:
		// createResponseUnitTestRequestDynamicVariables.Str is populated
	case components.CreateResponseUnitTestRequestDynamicVariablesTypeNumber:
		// createResponseUnitTestRequestDynamicVariables.Number is populated
	case components.CreateResponseUnitTestRequestDynamicVariablesTypeInteger:
		// createResponseUnitTestRequestDynamicVariables.Integer is populated
	case components.CreateResponseUnitTestRequestDynamicVariablesTypeBoolean:
		// createResponseUnitTestRequestDynamicVariables.Boolean is populated
}
```
