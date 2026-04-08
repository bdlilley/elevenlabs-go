# PhoneNumberTransferPostDialDigits


## Supported Types

### PostDialDigitsDynamicVariable

```go
phoneNumberTransferPostDialDigits := components.CreatePhoneNumberTransferPostDialDigitsDynamic(components.PostDialDigitsDynamicVariable{/* values here */})
```

### PostDialDigitsStatic

```go
phoneNumberTransferPostDialDigits := components.CreatePhoneNumberTransferPostDialDigitsStatic(components.PostDialDigitsStatic{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch phoneNumberTransferPostDialDigits.Type {
	case components.PhoneNumberTransferPostDialDigitsTypeDynamic:
		// phoneNumberTransferPostDialDigits.PostDialDigitsDynamicVariable is populated
	case components.PhoneNumberTransferPostDialDigitsTypeStatic:
		// phoneNumberTransferPostDialDigits.PostDialDigitsStatic is populated
	default:
		// Unknown type - use phoneNumberTransferPostDialDigits.GetUnknownRaw() for raw JSON
}
```
