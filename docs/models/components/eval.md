# Eval


## Supported Types

### MatchAnythingParameterEvaluationStrategy

```go
eval := components.CreateEvalAnything(components.MatchAnythingParameterEvaluationStrategy{/* values here */})
```

### ExactParameterEvaluationStrategy

```go
eval := components.CreateEvalExact(components.ExactParameterEvaluationStrategy{/* values here */})
```

### LLMParameterEvaluationStrategy

```go
eval := components.CreateEvalLlm(components.LLMParameterEvaluationStrategy{/* values here */})
```

### RegexParameterEvaluationStrategy

```go
eval := components.CreateEvalRegex(components.RegexParameterEvaluationStrategy{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch eval.Type {
	case components.EvalTypeAnything:
		// eval.MatchAnythingParameterEvaluationStrategy is populated
	case components.EvalTypeExact:
		// eval.ExactParameterEvaluationStrategy is populated
	case components.EvalTypeLlm:
		// eval.LLMParameterEvaluationStrategy is populated
	case components.EvalTypeRegex:
		// eval.RegexParameterEvaluationStrategy is populated
}
```
