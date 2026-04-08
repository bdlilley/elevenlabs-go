# GetResponseUnitTestResponseModelDynamicVariables


## Supported Types

### 

```go
getResponseUnitTestResponseModelDynamicVariables := components.CreateGetResponseUnitTestResponseModelDynamicVariablesStr(string{/* values here */})
```

### 

```go
getResponseUnitTestResponseModelDynamicVariables := components.CreateGetResponseUnitTestResponseModelDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
getResponseUnitTestResponseModelDynamicVariables := components.CreateGetResponseUnitTestResponseModelDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
getResponseUnitTestResponseModelDynamicVariables := components.CreateGetResponseUnitTestResponseModelDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getResponseUnitTestResponseModelDynamicVariables.Type {
	case components.GetResponseUnitTestResponseModelDynamicVariablesTypeStr:
		// getResponseUnitTestResponseModelDynamicVariables.Str is populated
	case components.GetResponseUnitTestResponseModelDynamicVariablesTypeNumber:
		// getResponseUnitTestResponseModelDynamicVariables.Number is populated
	case components.GetResponseUnitTestResponseModelDynamicVariablesTypeInteger:
		// getResponseUnitTestResponseModelDynamicVariables.Integer is populated
	case components.GetResponseUnitTestResponseModelDynamicVariablesTypeBoolean:
		// getResponseUnitTestResponseModelDynamicVariables.Boolean is populated
	default:
		// Unknown type - use getResponseUnitTestResponseModelDynamicVariables.GetUnknownRaw() for raw JSON
}
```
