# PhoneNumberTransferCustomSipHeader


## Supported Types

### CustomSIPHeaderWithDynamicVariable

```go
phoneNumberTransferCustomSipHeader := components.CreatePhoneNumberTransferCustomSipHeaderDynamic(components.CustomSIPHeaderWithDynamicVariable{/* values here */})
```

### CustomSIPHeader

```go
phoneNumberTransferCustomSipHeader := components.CreatePhoneNumberTransferCustomSipHeaderStatic(components.CustomSIPHeader{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch phoneNumberTransferCustomSipHeader.Type {
	case components.PhoneNumberTransferCustomSipHeaderTypeDynamic:
		// phoneNumberTransferCustomSipHeader.CustomSIPHeaderWithDynamicVariable is populated
	case components.PhoneNumberTransferCustomSipHeaderTypeStatic:
		// phoneNumberTransferCustomSipHeader.CustomSIPHeader is populated
	default:
		// Unknown type - use phoneNumberTransferCustomSipHeader.GetUnknownRaw() for raw JSON
}
```
