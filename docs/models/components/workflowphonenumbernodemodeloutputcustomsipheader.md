# WorkflowPhoneNumberNodeModelOutputCustomSipHeader


## Supported Types

### CustomSIPHeaderWithDynamicVariable

```go
workflowPhoneNumberNodeModelOutputCustomSipHeader := components.CreateWorkflowPhoneNumberNodeModelOutputCustomSipHeaderDynamic(components.CustomSIPHeaderWithDynamicVariable{/* values here */})
```

### CustomSIPHeader

```go
workflowPhoneNumberNodeModelOutputCustomSipHeader := components.CreateWorkflowPhoneNumberNodeModelOutputCustomSipHeaderStatic(components.CustomSIPHeader{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowPhoneNumberNodeModelOutputCustomSipHeader.Type {
	case components.WorkflowPhoneNumberNodeModelOutputCustomSipHeaderTypeDynamic:
		// workflowPhoneNumberNodeModelOutputCustomSipHeader.CustomSIPHeaderWithDynamicVariable is populated
	case components.WorkflowPhoneNumberNodeModelOutputCustomSipHeaderTypeStatic:
		// workflowPhoneNumberNodeModelOutputCustomSipHeader.CustomSIPHeader is populated
	default:
		// Unknown type - use workflowPhoneNumberNodeModelOutputCustomSipHeader.GetUnknownRaw() for raw JSON
}
```
