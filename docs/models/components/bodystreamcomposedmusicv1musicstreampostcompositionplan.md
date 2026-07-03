# BodyStreamComposedMusicV1MusicStreamPostCompositionPlan


## Supported Types

### MusicPrompt

```go
bodyStreamComposedMusicV1MusicStreamPostCompositionPlan := components.CreateBodyStreamComposedMusicV1MusicStreamPostCompositionPlanMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
bodyStreamComposedMusicV1MusicStreamPostCompositionPlan := components.CreateBodyStreamComposedMusicV1MusicStreamPostCompositionPlanCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyStreamComposedMusicV1MusicStreamPostCompositionPlan.Type {
	case components.BodyStreamComposedMusicV1MusicStreamPostCompositionPlanTypeMusicPrompt:
		// bodyStreamComposedMusicV1MusicStreamPostCompositionPlan.MusicPrompt is populated
	case components.BodyStreamComposedMusicV1MusicStreamPostCompositionPlanTypeCompositionPlan:
		// bodyStreamComposedMusicV1MusicStreamPostCompositionPlan.CompositionPlan is populated
}
```
