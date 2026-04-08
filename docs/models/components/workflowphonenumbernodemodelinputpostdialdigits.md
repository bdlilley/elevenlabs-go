# WorkflowPhoneNumberNodeModelInputPostDialDigits


## Supported Types

### PostDialDigitsDynamicVariable

```go
workflowPhoneNumberNodeModelInputPostDialDigits := components.CreateWorkflowPhoneNumberNodeModelInputPostDialDigitsDynamic(components.PostDialDigitsDynamicVariable{/* values here */})
```

### PostDialDigitsStatic

```go
workflowPhoneNumberNodeModelInputPostDialDigits := components.CreateWorkflowPhoneNumberNodeModelInputPostDialDigitsStatic(components.PostDialDigitsStatic{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowPhoneNumberNodeModelInputPostDialDigits.Type {
	case components.WorkflowPhoneNumberNodeModelInputPostDialDigitsTypeDynamic:
		// workflowPhoneNumberNodeModelInputPostDialDigits.PostDialDigitsDynamicVariable is populated
	case components.WorkflowPhoneNumberNodeModelInputPostDialDigitsTypeStatic:
		// workflowPhoneNumberNodeModelInputPostDialDigits.PostDialDigitsStatic is populated
}
```
