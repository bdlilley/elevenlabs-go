# BodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlan


## Supported Types

### MusicPrompt

```go
bodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlan := components.CreateBodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlanMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
bodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlan := components.CreateBodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlanCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlan.Type {
	case components.BodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlanTypeMusicPrompt:
		// bodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlan.MusicPrompt is populated
	case components.BodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlanTypeCompositionPlan:
		// bodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlan.CompositionPlan is populated
}
```
