# WorkflowPhoneNumberNodeModelOutputTransferDestination


## Supported Types

### PhoneNumberTransferDestination

```go
workflowPhoneNumberNodeModelOutputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelOutputTransferDestinationPhone(components.PhoneNumberTransferDestination{/* values here */})
```

### PhoneNumberDynamicVariableTransferDestination

```go
workflowPhoneNumberNodeModelOutputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelOutputTransferDestinationPhoneDynamicVariable(components.PhoneNumberDynamicVariableTransferDestination{/* values here */})
```

### SIPURITransferDestination

```go
workflowPhoneNumberNodeModelOutputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelOutputTransferDestinationSipURI(components.SIPURITransferDestination{/* values here */})
```

### SIPURIDynamicVariableTransferDestination

```go
workflowPhoneNumberNodeModelOutputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelOutputTransferDestinationSipURIDynamicVariable(components.SIPURIDynamicVariableTransferDestination{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowPhoneNumberNodeModelOutputTransferDestination.Type {
	case components.WorkflowPhoneNumberNodeModelOutputTransferDestinationTypePhone:
		// workflowPhoneNumberNodeModelOutputTransferDestination.PhoneNumberTransferDestination is populated
	case components.WorkflowPhoneNumberNodeModelOutputTransferDestinationTypePhoneDynamicVariable:
		// workflowPhoneNumberNodeModelOutputTransferDestination.PhoneNumberDynamicVariableTransferDestination is populated
	case components.WorkflowPhoneNumberNodeModelOutputTransferDestinationTypeSipURI:
		// workflowPhoneNumberNodeModelOutputTransferDestination.SIPURITransferDestination is populated
	case components.WorkflowPhoneNumberNodeModelOutputTransferDestinationTypeSipURIDynamicVariable:
		// workflowPhoneNumberNodeModelOutputTransferDestination.SIPURIDynamicVariableTransferDestination is populated
	default:
		// Unknown type - use workflowPhoneNumberNodeModelOutputTransferDestination.GetUnknownRaw() for raw JSON
}
```
