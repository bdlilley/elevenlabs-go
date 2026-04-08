# BodyAddVoiceV1VoicesAddPostLabels

Labels for the voice. Keys can be language, accent, gender, or age.


## Supported Types

### 

```go
bodyAddVoiceV1VoicesAddPostLabels := components.CreateBodyAddVoiceV1VoicesAddPostLabelsMapOfStr(map[string]string{/* values here */})
```

### 

```go
bodyAddVoiceV1VoicesAddPostLabels := components.CreateBodyAddVoiceV1VoicesAddPostLabelsStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyAddVoiceV1VoicesAddPostLabels.Type {
	case components.BodyAddVoiceV1VoicesAddPostLabelsTypeMapOfStr:
		// bodyAddVoiceV1VoicesAddPostLabels.MapOfStr is populated
	case components.BodyAddVoiceV1VoicesAddPostLabelsTypeStr:
		// bodyAddVoiceV1VoicesAddPostLabels.Str is populated
}
```
