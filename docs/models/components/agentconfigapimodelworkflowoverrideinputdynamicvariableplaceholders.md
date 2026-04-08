# AgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders


## Supported Types

### 

```go
agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersStr(string{/* values here */})
```

### 

```go
agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersNumber(float64{/* values here */})
```

### 

```go
agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersInteger(int64{/* values here */})
```

### 

```go
agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders.Type {
	case components.AgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersTypeStr:
		// agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders.Str is populated
	case components.AgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersTypeNumber:
		// agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders.Number is populated
	case components.AgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersTypeInteger:
		// agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders.Integer is populated
	case components.AgentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholdersTypeBoolean:
		// agentConfigAPIModelWorkflowOverrideInputDynamicVariablePlaceholders.Boolean is populated
}
```
