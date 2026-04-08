# DynamicVariablesConfigDynamicVariablePlaceholders


## Supported Types

### 

```go
dynamicVariablesConfigDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigDynamicVariablePlaceholdersStr(string{/* values here */})
```

### 

```go
dynamicVariablesConfigDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigDynamicVariablePlaceholdersNumber(float64{/* values here */})
```

### 

```go
dynamicVariablesConfigDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigDynamicVariablePlaceholdersInteger(int64{/* values here */})
```

### 

```go
dynamicVariablesConfigDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigDynamicVariablePlaceholdersBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch dynamicVariablesConfigDynamicVariablePlaceholders.Type {
	case components.DynamicVariablesConfigDynamicVariablePlaceholdersTypeStr:
		// dynamicVariablesConfigDynamicVariablePlaceholders.Str is populated
	case components.DynamicVariablesConfigDynamicVariablePlaceholdersTypeNumber:
		// dynamicVariablesConfigDynamicVariablePlaceholders.Number is populated
	case components.DynamicVariablesConfigDynamicVariablePlaceholdersTypeInteger:
		// dynamicVariablesConfigDynamicVariablePlaceholders.Integer is populated
	case components.DynamicVariablesConfigDynamicVariablePlaceholdersTypeBoolean:
		// dynamicVariablesConfigDynamicVariablePlaceholders.Boolean is populated
	default:
		// Unknown type - use dynamicVariablesConfigDynamicVariablePlaceholders.GetUnknownRaw() for raw JSON
}
```
