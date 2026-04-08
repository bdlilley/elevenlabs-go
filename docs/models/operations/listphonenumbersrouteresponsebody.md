# ListPhoneNumbersRouteResponseBody


## Supported Types

### GetPhoneNumberTwilioResponseModel

```go
listPhoneNumbersRouteResponseBody := operations.CreateListPhoneNumbersRouteResponseBodyTwilio(components.GetPhoneNumberTwilioResponseModel{/* values here */})
```

### GetPhoneNumberSIPTrunkResponseModel

```go
listPhoneNumbersRouteResponseBody := operations.CreateListPhoneNumbersRouteResponseBodySipTrunk(components.GetPhoneNumberSIPTrunkResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch listPhoneNumbersRouteResponseBody.Type {
	case operations.ListPhoneNumbersRouteResponseBodyTypeTwilio:
		// listPhoneNumbersRouteResponseBody.GetPhoneNumberTwilioResponseModel is populated
	case operations.ListPhoneNumbersRouteResponseBodyTypeSipTrunk:
		// listPhoneNumbersRouteResponseBody.GetPhoneNumberSIPTrunkResponseModel is populated
}
```
