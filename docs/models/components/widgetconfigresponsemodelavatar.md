# WidgetConfigResponseModelAvatar

The avatar of the widget


## Supported Types

### OrbAvatar

```go
widgetConfigResponseModelAvatar := components.CreateWidgetConfigResponseModelAvatarOrbAvatar(components.OrbAvatar{/* values here */})
```

### URLAvatar

```go
widgetConfigResponseModelAvatar := components.CreateWidgetConfigResponseModelAvatarURLAvatar(components.URLAvatar{/* values here */})
```

### ImageAvatar

```go
widgetConfigResponseModelAvatar := components.CreateWidgetConfigResponseModelAvatarImageAvatar(components.ImageAvatar{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch widgetConfigResponseModelAvatar.Type {
	case components.WidgetConfigResponseModelAvatarTypeOrbAvatar:
		// widgetConfigResponseModelAvatar.OrbAvatar is populated
	case components.WidgetConfigResponseModelAvatarTypeURLAvatar:
		// widgetConfigResponseModelAvatar.URLAvatar is populated
	case components.WidgetConfigResponseModelAvatarTypeImageAvatar:
		// widgetConfigResponseModelAvatar.ImageAvatar is populated
	default:
		// Unknown type - use widgetConfigResponseModelAvatar.GetUnknownRaw() for raw JSON
}
```
