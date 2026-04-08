# ConversationInitiationClientDataRequestInputDynamicVariables


## Supported Types

### 

```go
conversationInitiationClientDataRequestInputDynamicVariables := components.CreateConversationInitiationClientDataRequestInputDynamicVariablesStr(string{/* values here */})
```

### 

```go
conversationInitiationClientDataRequestInputDynamicVariables := components.CreateConversationInitiationClientDataRequestInputDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
conversationInitiationClientDataRequestInputDynamicVariables := components.CreateConversationInitiationClientDataRequestInputDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
conversationInitiationClientDataRequestInputDynamicVariables := components.CreateConversationInitiationClientDataRequestInputDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch conversationInitiationClientDataRequestInputDynamicVariables.Type {
	case components.ConversationInitiationClientDataRequestInputDynamicVariablesTypeStr:
		// conversationInitiationClientDataRequestInputDynamicVariables.Str is populated
	case components.ConversationInitiationClientDataRequestInputDynamicVariablesTypeNumber:
		// conversationInitiationClientDataRequestInputDynamicVariables.Number is populated
	case components.ConversationInitiationClientDataRequestInputDynamicVariablesTypeInteger:
		// conversationInitiationClientDataRequestInputDynamicVariables.Integer is populated
	case components.ConversationInitiationClientDataRequestInputDynamicVariablesTypeBoolean:
		// conversationInitiationClientDataRequestInputDynamicVariables.Boolean is populated
}
```
