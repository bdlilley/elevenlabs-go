# WorkflowPhoneNumberNodeModelInputTransferDestination


## Supported Types

### PhoneNumberTransferDestination

```go
workflowPhoneNumberNodeModelInputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationPhone(components.PhoneNumberTransferDestination{/* values here */})
```

### PhoneNumberDynamicVariableTransferDestination

```go
workflowPhoneNumberNodeModelInputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationPhoneDynamicVariable(components.PhoneNumberDynamicVariableTransferDestination{/* values here */})
```

### SIPURITransferDestination

```go
workflowPhoneNumberNodeModelInputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationSipURI(components.SIPURITransferDestination{/* values here */})
```

### SIPURIDynamicVariableTransferDestination

```go
workflowPhoneNumberNodeModelInputTransferDestination := components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationSipURIDynamicVariable(components.SIPURIDynamicVariableTransferDestination{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowPhoneNumberNodeModelInputTransferDestination.Type {
	case components.WorkflowPhoneNumberNodeModelInputTransferDestinationTypePhone:
		// workflowPhoneNumberNodeModelInputTransferDestination.PhoneNumberTransferDestination is populated
	case components.WorkflowPhoneNumberNodeModelInputTransferDestinationTypePhoneDynamicVariable:
		// workflowPhoneNumberNodeModelInputTransferDestination.PhoneNumberDynamicVariableTransferDestination is populated
	case components.WorkflowPhoneNumberNodeModelInputTransferDestinationTypeSipURI:
		// workflowPhoneNumberNodeModelInputTransferDestination.SIPURITransferDestination is populated
	case components.WorkflowPhoneNumberNodeModelInputTransferDestinationTypeSipURIDynamicVariable:
		// workflowPhoneNumberNodeModelInputTransferDestination.SIPURIDynamicVariableTransferDestination is populated
}
```
