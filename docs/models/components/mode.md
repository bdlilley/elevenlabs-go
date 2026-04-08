# Mode

The type of podcast to generate. Can be 'conversation', an interaction between two voices, or 'bulletin', a monologue.


## Supported Types

### PodcastConversationMode

```go
mode := components.CreateModeConversation(components.PodcastConversationMode{/* values here */})
```

### PodcastBulletinMode

```go
mode := components.CreateModeBulletin(components.PodcastBulletinMode{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mode.Type {
	case components.ModeTypeConversation:
		// mode.PodcastConversationMode is populated
	case components.ModeTypeBulletin:
		// mode.PodcastBulletinMode is populated
}
```
