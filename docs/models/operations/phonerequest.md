# PhoneRequest

Create Phone Request Information


## Supported Types

### CreateTwilioPhoneNumberRequest

```go
phoneRequest := operations.CreatePhoneRequestCreateTwilioPhoneNumberRequest(components.CreateTwilioPhoneNumberRequest{/* values here */})
```

### CreateSIPTrunkPhoneNumberRequestV2

```go
phoneRequest := operations.CreatePhoneRequestCreateSIPTrunkPhoneNumberRequestV2(components.CreateSIPTrunkPhoneNumberRequestV2{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch phoneRequest.Type {
	case operations.PhoneRequestTypeCreateTwilioPhoneNumberRequest:
		// phoneRequest.CreateTwilioPhoneNumberRequest is populated
	case operations.PhoneRequestTypeCreateSIPTrunkPhoneNumberRequestV2:
		// phoneRequest.CreateSIPTrunkPhoneNumberRequestV2 is populated
}
```
