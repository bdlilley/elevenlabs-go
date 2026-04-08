# WidgetConfigOutputAvatar

The avatar of the widget


## Supported Types

### OrbAvatar

```go
widgetConfigOutputAvatar := components.CreateWidgetConfigOutputAvatarOrbAvatar(components.OrbAvatar{/* values here */})
```

### URLAvatar

```go
widgetConfigOutputAvatar := components.CreateWidgetConfigOutputAvatarURLAvatar(components.URLAvatar{/* values here */})
```

### ImageAvatar

```go
widgetConfigOutputAvatar := components.CreateWidgetConfigOutputAvatarImageAvatar(components.ImageAvatar{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch widgetConfigOutputAvatar.Type {
	case components.WidgetConfigOutputAvatarTypeOrbAvatar:
		// widgetConfigOutputAvatar.OrbAvatar is populated
	case components.WidgetConfigOutputAvatarTypeURLAvatar:
		// widgetConfigOutputAvatar.URLAvatar is populated
	case components.WidgetConfigOutputAvatarTypeImageAvatar:
		// widgetConfigOutputAvatar.ImageAvatar is populated
}
```
