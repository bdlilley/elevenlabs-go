# BodyEditVoiceV1VoicesVoiceIDEditPostLabels

Labels for the voice. Keys can be language, accent, gender, or age.


## Supported Types

### 

```go
bodyEditVoiceV1VoicesVoiceIDEditPostLabels := components.CreateBodyEditVoiceV1VoicesVoiceIDEditPostLabelsMapOfStr(map[string]string{/* values here */})
```

### 

```go
bodyEditVoiceV1VoicesVoiceIDEditPostLabels := components.CreateBodyEditVoiceV1VoicesVoiceIDEditPostLabelsStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyEditVoiceV1VoicesVoiceIDEditPostLabels.Type {
	case components.BodyEditVoiceV1VoicesVoiceIDEditPostLabelsTypeMapOfStr:
		// bodyEditVoiceV1VoicesVoiceIDEditPostLabels.MapOfStr is populated
	case components.BodyEditVoiceV1VoicesVoiceIDEditPostLabelsTypeStr:
		// bodyEditVoiceV1VoicesVoiceIDEditPostLabels.Str is populated
}
```
