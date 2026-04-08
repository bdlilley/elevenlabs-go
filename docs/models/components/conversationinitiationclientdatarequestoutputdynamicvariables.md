# ConversationInitiationClientDataRequestOutputDynamicVariables


## Supported Types

### 

```go
conversationInitiationClientDataRequestOutputDynamicVariables := components.CreateConversationInitiationClientDataRequestOutputDynamicVariablesStr(string{/* values here */})
```

### 

```go
conversationInitiationClientDataRequestOutputDynamicVariables := components.CreateConversationInitiationClientDataRequestOutputDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
conversationInitiationClientDataRequestOutputDynamicVariables := components.CreateConversationInitiationClientDataRequestOutputDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
conversationInitiationClientDataRequestOutputDynamicVariables := components.CreateConversationInitiationClientDataRequestOutputDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch conversationInitiationClientDataRequestOutputDynamicVariables.Type {
	case components.ConversationInitiationClientDataRequestOutputDynamicVariablesTypeStr:
		// conversationInitiationClientDataRequestOutputDynamicVariables.Str is populated
	case components.ConversationInitiationClientDataRequestOutputDynamicVariablesTypeNumber:
		// conversationInitiationClientDataRequestOutputDynamicVariables.Number is populated
	case components.ConversationInitiationClientDataRequestOutputDynamicVariablesTypeInteger:
		// conversationInitiationClientDataRequestOutputDynamicVariables.Integer is populated
	case components.ConversationInitiationClientDataRequestOutputDynamicVariablesTypeBoolean:
		// conversationInitiationClientDataRequestOutputDynamicVariables.Boolean is populated
}
```
