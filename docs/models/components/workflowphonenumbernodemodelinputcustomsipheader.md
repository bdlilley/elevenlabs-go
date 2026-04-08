# WorkflowPhoneNumberNodeModelInputCustomSipHeader


## Supported Types

### CustomSIPHeaderWithDynamicVariable

```go
workflowPhoneNumberNodeModelInputCustomSipHeader := components.CreateWorkflowPhoneNumberNodeModelInputCustomSipHeaderDynamic(components.CustomSIPHeaderWithDynamicVariable{/* values here */})
```

### CustomSIPHeader

```go
workflowPhoneNumberNodeModelInputCustomSipHeader := components.CreateWorkflowPhoneNumberNodeModelInputCustomSipHeaderStatic(components.CustomSIPHeader{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowPhoneNumberNodeModelInputCustomSipHeader.Type {
	case components.WorkflowPhoneNumberNodeModelInputCustomSipHeaderTypeDynamic:
		// workflowPhoneNumberNodeModelInputCustomSipHeader.CustomSIPHeaderWithDynamicVariable is populated
	case components.WorkflowPhoneNumberNodeModelInputCustomSipHeaderTypeStatic:
		// workflowPhoneNumberNodeModelInputCustomSipHeader.CustomSIPHeader is populated
}
```
