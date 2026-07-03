# ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet

Successful Response


## Supported Types

### GetPhoneNumberTwilioResponseModel

```go
responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet := operations.CreateResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTwilio(components.GetPhoneNumberTwilioResponseModel{/* values here */})
```

### GetPhoneNumberExotelResponseModel

```go
responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet := operations.CreateResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetExotel(components.GetPhoneNumberExotelResponseModel{/* values here */})
```

### GetPhoneNumberSIPTrunkResponseModel

```go
responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet := operations.CreateResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetSipTrunk(components.GetPhoneNumberSIPTrunkResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.Type {
	case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeTwilio:
		// responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberTwilioResponseModel is populated
	case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeExotel:
		// responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberExotelResponseModel is populated
	case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeSipTrunk:
		// responseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberSIPTrunkResponseModel is populated
}
```
