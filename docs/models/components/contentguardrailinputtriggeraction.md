# ContentGuardrailInputTriggerAction


## Supported Types

### EndCallTriggerAction

```go
contentGuardrailInputTriggerAction := components.CreateContentGuardrailInputTriggerActionEndCall(components.EndCallTriggerAction{/* values here */})
```

### RetryTriggerAction

```go
contentGuardrailInputTriggerAction := components.CreateContentGuardrailInputTriggerActionRetry(components.RetryTriggerAction{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch contentGuardrailInputTriggerAction.Type {
	case components.ContentGuardrailInputTriggerActionTypeEndCall:
		// contentGuardrailInputTriggerAction.EndCallTriggerAction is populated
	case components.ContentGuardrailInputTriggerActionTypeRetry:
		// contentGuardrailInputTriggerAction.RetryTriggerAction is populated
}
```
