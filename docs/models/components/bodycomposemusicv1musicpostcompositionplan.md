# BodyComposeMusicV1MusicPostCompositionPlan


## Supported Types

### MusicPrompt

```go
bodyComposeMusicV1MusicPostCompositionPlan := components.CreateBodyComposeMusicV1MusicPostCompositionPlanMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
bodyComposeMusicV1MusicPostCompositionPlan := components.CreateBodyComposeMusicV1MusicPostCompositionPlanCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyComposeMusicV1MusicPostCompositionPlan.Type {
	case components.BodyComposeMusicV1MusicPostCompositionPlanTypeMusicPrompt:
		// bodyComposeMusicV1MusicPostCompositionPlan.MusicPrompt is populated
	case components.BodyComposeMusicV1MusicPostCompositionPlanTypeCompositionPlan:
		// bodyComposeMusicV1MusicPostCompositionPlan.CompositionPlan is populated
}
```
