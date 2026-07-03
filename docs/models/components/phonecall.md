# PhoneCall


## Supported Types

### ConversationHistoryExotelPhoneCallModel

```go
phoneCall := components.CreatePhoneCallExotel(components.ConversationHistoryExotelPhoneCallModel{/* values here */})
```

### ConversationHistorySIPTrunkingPhoneCallModel

```go
phoneCall := components.CreatePhoneCallSipTrunking(components.ConversationHistorySIPTrunkingPhoneCallModel{/* values here */})
```

### ConversationHistoryTwilioPhoneCallModel

```go
phoneCall := components.CreatePhoneCallTwilio(components.ConversationHistoryTwilioPhoneCallModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch phoneCall.Type {
	case components.PhoneCallTypeExotel:
		// phoneCall.ConversationHistoryExotelPhoneCallModel is populated
	case components.PhoneCallTypeSipTrunking:
		// phoneCall.ConversationHistorySIPTrunkingPhoneCallModel is populated
	case components.PhoneCallTypeTwilio:
		// phoneCall.ConversationHistoryTwilioPhoneCallModel is populated
}
```
