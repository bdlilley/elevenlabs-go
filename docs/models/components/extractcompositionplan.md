# ExtractCompositionPlan

Whether to generate and return the composition plan for the uploaded song. Pass a model id (`music_v1` or `music_v2`) to control which composition plan format is returned. Passing `true`/`false` is deprecated; `true` defaults to the `music_v1` plan format. Enabling this will increase the latency.


## Supported Types

### 

```go
extractCompositionPlan := components.CreateExtractCompositionPlanBoolean(bool{/* values here */})
```

### ExtractCompositionPlanEnum

```go
extractCompositionPlan := components.CreateExtractCompositionPlanExtractCompositionPlanEnum(components.ExtractCompositionPlanEnum{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch extractCompositionPlan.Type {
	case components.ExtractCompositionPlanTypeBoolean:
		// extractCompositionPlan.Boolean is populated
	case components.ExtractCompositionPlanTypeExtractCompositionPlanEnum:
		// extractCompositionPlan.ExtractCompositionPlanEnum is populated
}
```
