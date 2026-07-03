# SourceCompositionPlan

An optional composition plan to use as a source for the new composition plan.


## Supported Types

### MusicPrompt

```go
sourceCompositionPlan := components.CreateSourceCompositionPlanMusicPrompt(components.MusicPrompt{/* values here */})
```

### CompositionPlan

```go
sourceCompositionPlan := components.CreateSourceCompositionPlanCompositionPlan(components.CompositionPlan{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch sourceCompositionPlan.Type {
	case components.SourceCompositionPlanTypeMusicPrompt:
		// sourceCompositionPlan.MusicPrompt is populated
	case components.SourceCompositionPlanTypeCompositionPlan:
		// sourceCompositionPlan.CompositionPlan is populated
}
```
