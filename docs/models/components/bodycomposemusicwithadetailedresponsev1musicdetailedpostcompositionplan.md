# BodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlan


## Supported Types

### MusicPrompt

```go
bodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlan := components.CreateBodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlanMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
bodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlan := components.CreateBodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlanCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlan.Type {
	case components.BodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlanTypeMusicPrompt:
		// bodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlan.MusicPrompt is populated
	case components.BodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlanTypeCompositionPlan:
		// bodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlan.CompositionPlan is populated
}
```
