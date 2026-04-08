# ContentGuardrailOutputTriggerAction


## Supported Types

### EndCallTriggerAction

```go
contentGuardrailOutputTriggerAction := components.CreateContentGuardrailOutputTriggerActionEndCall(components.EndCallTriggerAction{/* values here */})
```

### RetryTriggerAction

```go
contentGuardrailOutputTriggerAction := components.CreateContentGuardrailOutputTriggerActionRetry(components.RetryTriggerAction{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch contentGuardrailOutputTriggerAction.Type {
	case components.ContentGuardrailOutputTriggerActionTypeEndCall:
		// contentGuardrailOutputTriggerAction.EndCallTriggerAction is populated
	case components.ContentGuardrailOutputTriggerActionTypeRetry:
		// contentGuardrailOutputTriggerAction.RetryTriggerAction is populated
	default:
		// Unknown type - use contentGuardrailOutputTriggerAction.GetUnknownRaw() for raw JSON
}
```
