# PhoneNumberTransferTransferDestination


## Supported Types

### PhoneNumberTransferDestination

```go
phoneNumberTransferTransferDestination := components.CreatePhoneNumberTransferTransferDestinationPhone(components.PhoneNumberTransferDestination{/* values here */})
```

### PhoneNumberDynamicVariableTransferDestination

```go
phoneNumberTransferTransferDestination := components.CreatePhoneNumberTransferTransferDestinationPhoneDynamicVariable(components.PhoneNumberDynamicVariableTransferDestination{/* values here */})
```

### SIPURITransferDestination

```go
phoneNumberTransferTransferDestination := components.CreatePhoneNumberTransferTransferDestinationSipURI(components.SIPURITransferDestination{/* values here */})
```

### SIPURIDynamicVariableTransferDestination

```go
phoneNumberTransferTransferDestination := components.CreatePhoneNumberTransferTransferDestinationSipURIDynamicVariable(components.SIPURIDynamicVariableTransferDestination{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch phoneNumberTransferTransferDestination.Type {
	case components.PhoneNumberTransferTransferDestinationTypePhone:
		// phoneNumberTransferTransferDestination.PhoneNumberTransferDestination is populated
	case components.PhoneNumberTransferTransferDestinationTypePhoneDynamicVariable:
		// phoneNumberTransferTransferDestination.PhoneNumberDynamicVariableTransferDestination is populated
	case components.PhoneNumberTransferTransferDestinationTypeSipURI:
		// phoneNumberTransferTransferDestination.SIPURITransferDestination is populated
	case components.PhoneNumberTransferTransferDestinationTypeSipURIDynamicVariable:
		// phoneNumberTransferTransferDestination.SIPURIDynamicVariableTransferDestination is populated
}
```
