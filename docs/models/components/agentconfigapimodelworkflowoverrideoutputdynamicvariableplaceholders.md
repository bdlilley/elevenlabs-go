# AgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders


## Supported Types

### 

```go
agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersStr(string{/* values here */})
```

### 

```go
agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersNumber(float64{/* values here */})
```

### 

```go
agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersInteger(int64{/* values here */})
```

### 

```go
agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders := components.CreateAgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders.Type {
	case components.AgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersTypeStr:
		// agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders.Str is populated
	case components.AgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersTypeNumber:
		// agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders.Number is populated
	case components.AgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersTypeInteger:
		// agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders.Integer is populated
	case components.AgentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholdersTypeBoolean:
		// agentConfigAPIModelWorkflowOverrideOutputDynamicVariablePlaceholders.Boolean is populated
}
```
