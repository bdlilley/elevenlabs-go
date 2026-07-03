# MergePreviewResponseModelPhoneNumber


## Supported Types

### GetPhoneNumberExotelResponseModel

```go
mergePreviewResponseModelPhoneNumber := components.CreateMergePreviewResponseModelPhoneNumberExotel(components.GetPhoneNumberExotelResponseModel{/* values here */})
```

### GetPhoneNumberSIPTrunkResponseModel

```go
mergePreviewResponseModelPhoneNumber := components.CreateMergePreviewResponseModelPhoneNumberSipTrunk(components.GetPhoneNumberSIPTrunkResponseModel{/* values here */})
```

### GetPhoneNumberTwilioResponseModel

```go
mergePreviewResponseModelPhoneNumber := components.CreateMergePreviewResponseModelPhoneNumberTwilio(components.GetPhoneNumberTwilioResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mergePreviewResponseModelPhoneNumber.Type {
	case components.MergePreviewResponseModelPhoneNumberTypeExotel:
		// mergePreviewResponseModelPhoneNumber.GetPhoneNumberExotelResponseModel is populated
	case components.MergePreviewResponseModelPhoneNumberTypeSipTrunk:
		// mergePreviewResponseModelPhoneNumber.GetPhoneNumberSIPTrunkResponseModel is populated
	case components.MergePreviewResponseModelPhoneNumberTypeTwilio:
		// mergePreviewResponseModelPhoneNumber.GetPhoneNumberTwilioResponseModel is populated
}
```
