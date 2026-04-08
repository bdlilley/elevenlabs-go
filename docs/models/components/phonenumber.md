# PhoneNumber


## Supported Types

### GetPhoneNumberSIPTrunkResponseModel

```go
phoneNumber := components.CreatePhoneNumberSipTrunk(components.GetPhoneNumberSIPTrunkResponseModel{/* values here */})
```

### GetPhoneNumberTwilioResponseModel

```go
phoneNumber := components.CreatePhoneNumberTwilio(components.GetPhoneNumberTwilioResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch phoneNumber.Type {
	case components.PhoneNumberTypeSipTrunk:
		// phoneNumber.GetPhoneNumberSIPTrunkResponseModel is populated
	case components.PhoneNumberTypeTwilio:
		// phoneNumber.GetPhoneNumberTwilioResponseModel is populated
	default:
		// Unknown type - use phoneNumber.GetUnknownRaw() for raw JSON
}
```
