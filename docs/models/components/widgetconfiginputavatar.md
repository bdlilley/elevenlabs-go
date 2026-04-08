# WidgetConfigInputAvatar

The avatar of the widget


## Supported Types

### OrbAvatar

```go
widgetConfigInputAvatar := components.CreateWidgetConfigInputAvatarOrbAvatar(components.OrbAvatar{/* values here */})
```

### URLAvatar

```go
widgetConfigInputAvatar := components.CreateWidgetConfigInputAvatarURLAvatar(components.URLAvatar{/* values here */})
```

### ImageAvatar

```go
widgetConfigInputAvatar := components.CreateWidgetConfigInputAvatarImageAvatar(components.ImageAvatar{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch widgetConfigInputAvatar.Type {
	case components.WidgetConfigInputAvatarTypeOrbAvatar:
		// widgetConfigInputAvatar.OrbAvatar is populated
	case components.WidgetConfigInputAvatarTypeURLAvatar:
		// widgetConfigInputAvatar.URLAvatar is populated
	case components.WidgetConfigInputAvatarTypeImageAvatar:
		// widgetConfigInputAvatar.ImageAvatar is populated
}
```
