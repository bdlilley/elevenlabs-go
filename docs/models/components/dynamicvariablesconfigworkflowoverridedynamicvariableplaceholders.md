# DynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders


## Supported Types

### 

```go
dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersStr(string{/* values here */})
```

### 

```go
dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersNumber(float64{/* values here */})
```

### 

```go
dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersInteger(int64{/* values here */})
```

### 

```go
dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders := components.CreateDynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders.Type {
	case components.DynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersTypeStr:
		// dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders.Str is populated
	case components.DynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersTypeNumber:
		// dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders.Number is populated
	case components.DynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersTypeInteger:
		// dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders.Integer is populated
	case components.DynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholdersTypeBoolean:
		// dynamicVariablesConfigWorkflowOverrideDynamicVariablePlaceholders.Boolean is populated
}
```
