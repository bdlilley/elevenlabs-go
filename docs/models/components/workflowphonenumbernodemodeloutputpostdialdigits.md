# WorkflowPhoneNumberNodeModelOutputPostDialDigits


## Supported Types

### PostDialDigitsDynamicVariable

```go
workflowPhoneNumberNodeModelOutputPostDialDigits := components.CreateWorkflowPhoneNumberNodeModelOutputPostDialDigitsDynamic(components.PostDialDigitsDynamicVariable{/* values here */})
```

### PostDialDigitsStatic

```go
workflowPhoneNumberNodeModelOutputPostDialDigits := components.CreateWorkflowPhoneNumberNodeModelOutputPostDialDigitsStatic(components.PostDialDigitsStatic{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowPhoneNumberNodeModelOutputPostDialDigits.Type {
	case components.WorkflowPhoneNumberNodeModelOutputPostDialDigitsTypeDynamic:
		// workflowPhoneNumberNodeModelOutputPostDialDigits.PostDialDigitsDynamicVariable is populated
	case components.WorkflowPhoneNumberNodeModelOutputPostDialDigitsTypeStatic:
		// workflowPhoneNumberNodeModelOutputPostDialDigits.PostDialDigitsStatic is populated
}
```
