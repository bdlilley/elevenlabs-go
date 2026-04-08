# ResponseUnitTestModelDynamicVariables


## Supported Types

### 

```go
responseUnitTestModelDynamicVariables := components.CreateResponseUnitTestModelDynamicVariablesStr(string{/* values here */})
```

### 

```go
responseUnitTestModelDynamicVariables := components.CreateResponseUnitTestModelDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
responseUnitTestModelDynamicVariables := components.CreateResponseUnitTestModelDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
responseUnitTestModelDynamicVariables := components.CreateResponseUnitTestModelDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseUnitTestModelDynamicVariables.Type {
	case components.ResponseUnitTestModelDynamicVariablesTypeStr:
		// responseUnitTestModelDynamicVariables.Str is populated
	case components.ResponseUnitTestModelDynamicVariablesTypeNumber:
		// responseUnitTestModelDynamicVariables.Number is populated
	case components.ResponseUnitTestModelDynamicVariablesTypeInteger:
		// responseUnitTestModelDynamicVariables.Integer is populated
	case components.ResponseUnitTestModelDynamicVariablesTypeBoolean:
		// responseUnitTestModelDynamicVariables.Boolean is populated
	default:
		// Unknown type - use responseUnitTestModelDynamicVariables.GetUnknownRaw() for raw JSON
}
```
