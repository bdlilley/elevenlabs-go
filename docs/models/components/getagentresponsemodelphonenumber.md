# GetAgentResponseModelPhoneNumber


## Supported Types

### GetPhoneNumberExotelResponseModel

```go
getAgentResponseModelPhoneNumber := components.CreateGetAgentResponseModelPhoneNumberExotel(components.GetPhoneNumberExotelResponseModel{/* values here */})
```

### GetPhoneNumberSIPTrunkResponseModel

```go
getAgentResponseModelPhoneNumber := components.CreateGetAgentResponseModelPhoneNumberSipTrunk(components.GetPhoneNumberSIPTrunkResponseModel{/* values here */})
```

### GetPhoneNumberTwilioResponseModel

```go
getAgentResponseModelPhoneNumber := components.CreateGetAgentResponseModelPhoneNumberTwilio(components.GetPhoneNumberTwilioResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getAgentResponseModelPhoneNumber.Type {
	case components.GetAgentResponseModelPhoneNumberTypeExotel:
		// getAgentResponseModelPhoneNumber.GetPhoneNumberExotelResponseModel is populated
	case components.GetAgentResponseModelPhoneNumberTypeSipTrunk:
		// getAgentResponseModelPhoneNumber.GetPhoneNumberSIPTrunkResponseModel is populated
	case components.GetAgentResponseModelPhoneNumberTypeTwilio:
		// getAgentResponseModelPhoneNumber.GetPhoneNumberTwilioResponseModel is populated
}
```
