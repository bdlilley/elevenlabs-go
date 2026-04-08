# UpdateResponseUnitTestRequestDynamicVariables


## Supported Types

### 

```go
updateResponseUnitTestRequestDynamicVariables := components.CreateUpdateResponseUnitTestRequestDynamicVariablesStr(string{/* values here */})
```

### 

```go
updateResponseUnitTestRequestDynamicVariables := components.CreateUpdateResponseUnitTestRequestDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
updateResponseUnitTestRequestDynamicVariables := components.CreateUpdateResponseUnitTestRequestDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
updateResponseUnitTestRequestDynamicVariables := components.CreateUpdateResponseUnitTestRequestDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch updateResponseUnitTestRequestDynamicVariables.Type {
	case components.UpdateResponseUnitTestRequestDynamicVariablesTypeStr:
		// updateResponseUnitTestRequestDynamicVariables.Str is populated
	case components.UpdateResponseUnitTestRequestDynamicVariablesTypeNumber:
		// updateResponseUnitTestRequestDynamicVariables.Number is populated
	case components.UpdateResponseUnitTestRequestDynamicVariablesTypeInteger:
		// updateResponseUnitTestRequestDynamicVariables.Integer is populated
	case components.UpdateResponseUnitTestRequestDynamicVariablesTypeBoolean:
		// updateResponseUnitTestRequestDynamicVariables.Boolean is populated
}
```
