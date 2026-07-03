# MusicUploadResponseCompositionPlan

The composition plan extracted from the uploaded song. Only present if `extract_composition_plan` was provided in the request body.


## Supported Types

### MusicPrompt

```go
musicUploadResponseCompositionPlan := components.CreateMusicUploadResponseCompositionPlanMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
musicUploadResponseCompositionPlan := components.CreateMusicUploadResponseCompositionPlanCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch musicUploadResponseCompositionPlan.Type {
	case components.MusicUploadResponseCompositionPlanTypeMusicPrompt:
		// musicUploadResponseCompositionPlan.MusicPrompt is populated
	case components.MusicUploadResponseCompositionPlanTypeCompositionPlan:
		// musicUploadResponseCompositionPlan.CompositionPlan is populated
}
```
