# CustomGuardrailConfigTriggerAction


## Supported Types

### EndCallTriggerAction

```go
customGuardrailConfigTriggerAction := components.CreateCustomGuardrailConfigTriggerActionEndCall(components.EndCallTriggerAction{/* values here */})
```

### RetryTriggerAction

```go
customGuardrailConfigTriggerAction := components.CreateCustomGuardrailConfigTriggerActionRetry(components.RetryTriggerAction{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch customGuardrailConfigTriggerAction.Type {
	case components.CustomGuardrailConfigTriggerActionTypeEndCall:
		// customGuardrailConfigTriggerAction.EndCallTriggerAction is populated
	case components.CustomGuardrailConfigTriggerActionTypeRetry:
		// customGuardrailConfigTriggerAction.RetryTriggerAction is populated
	default:
		// Unknown type - use customGuardrailConfigTriggerAction.GetUnknownRaw() for raw JSON
}
```
