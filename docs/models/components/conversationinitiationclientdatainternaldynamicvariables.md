# ConversationInitiationClientDataInternalDynamicVariables


## Supported Types

### 

```go
conversationInitiationClientDataInternalDynamicVariables := components.CreateConversationInitiationClientDataInternalDynamicVariablesStr(string{/* values here */})
```

### 

```go
conversationInitiationClientDataInternalDynamicVariables := components.CreateConversationInitiationClientDataInternalDynamicVariablesNumber(float64{/* values here */})
```

### 

```go
conversationInitiationClientDataInternalDynamicVariables := components.CreateConversationInitiationClientDataInternalDynamicVariablesInteger(int64{/* values here */})
```

### 

```go
conversationInitiationClientDataInternalDynamicVariables := components.CreateConversationInitiationClientDataInternalDynamicVariablesBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch conversationInitiationClientDataInternalDynamicVariables.Type {
	case components.ConversationInitiationClientDataInternalDynamicVariablesTypeStr:
		// conversationInitiationClientDataInternalDynamicVariables.Str is populated
	case components.ConversationInitiationClientDataInternalDynamicVariablesTypeNumber:
		// conversationInitiationClientDataInternalDynamicVariables.Number is populated
	case components.ConversationInitiationClientDataInternalDynamicVariablesTypeInteger:
		// conversationInitiationClientDataInternalDynamicVariables.Integer is populated
	case components.ConversationInitiationClientDataInternalDynamicVariablesTypeBoolean:
		// conversationInitiationClientDataInternalDynamicVariables.Boolean is populated
}
```
