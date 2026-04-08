# ConversationSimulationSpecificationDynamicVariables


## Supported Types

### 

```go
conversationSimulationSpecificationDynamicVariables := components.CreateConversationSimulationSpecificationDynamicVariablesStr(string{/* values here */})
```

### 

```go
conversationSimulationSpecificationDynamicVariables := components.CreateConversationSimulationSpecificationDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
conversationSimulationSpecificationDynamicVariables := components.CreateConversationSimulationSpecificationDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
conversationSimulationSpecificationDynamicVariables := components.CreateConversationSimulationSpecificationDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch conversationSimulationSpecificationDynamicVariables.Type {
	case components.ConversationSimulationSpecificationDynamicVariablesTypeStr:
		// conversationSimulationSpecificationDynamicVariables.Str is populated
	case components.ConversationSimulationSpecificationDynamicVariablesTypeNumber:
		// conversationSimulationSpecificationDynamicVariables.Number is populated
	case components.ConversationSimulationSpecificationDynamicVariablesTypeInteger:
		// conversationSimulationSpecificationDynamicVariables.Integer is populated
	case components.ConversationSimulationSpecificationDynamicVariablesTypeBoolean:
		// conversationSimulationSpecificationDynamicVariables.Boolean is populated
}
```
