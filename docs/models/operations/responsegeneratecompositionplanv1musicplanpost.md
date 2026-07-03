# ResponseGenerateCompositionPlanV1MusicPlanPost

Successful Response


## Supported Types

### MusicPrompt

```go
responseGenerateCompositionPlanV1MusicPlanPost := operations.CreateResponseGenerateCompositionPlanV1MusicPlanPostMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
responseGenerateCompositionPlanV1MusicPlanPost := operations.CreateResponseGenerateCompositionPlanV1MusicPlanPostCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseGenerateCompositionPlanV1MusicPlanPost.Type {
	case operations.ResponseGenerateCompositionPlanV1MusicPlanPostTypeMusicPrompt:
		// responseGenerateCompositionPlanV1MusicPlanPost.MusicPrompt is populated
	case operations.ResponseGenerateCompositionPlanV1MusicPlanPostTypeCompositionPlan:
		// responseGenerateCompositionPlanV1MusicPlanPost.CompositionPlan is populated
}
```
