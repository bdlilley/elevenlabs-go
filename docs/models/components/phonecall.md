# PhoneCall


## Supported Types

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
	case components.PhoneCallTypeSipTrunking:
		// phoneCall.ConversationHistorySIPTrunkingPhoneCallModel is populated
	case components.PhoneCallTypeTwilio:
		// phoneCall.ConversationHistoryTwilioPhoneCallModel is populated
	default:
		// Unknown type - use phoneCall.GetUnknownRaw() for raw JSON
}
```
