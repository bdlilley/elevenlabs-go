# ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch

Successful Response


## Supported Types

### GetPhoneNumberTwilioResponseModel

```go
responseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch := operations.CreateResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTwilio(components.GetPhoneNumberTwilioResponseModel{/* values here */})
```

### GetPhoneNumberSIPTrunkResponseModel

```go
responseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch := operations.CreateResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchSipTrunk(components.GetPhoneNumberSIPTrunkResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.Type {
	case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeTwilio:
		// responseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberTwilioResponseModel is populated
	case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeSipTrunk:
		// responseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberSIPTrunkResponseModel is populated
}
```
