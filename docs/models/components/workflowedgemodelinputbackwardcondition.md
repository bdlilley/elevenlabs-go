# WorkflowEdgeModelInputBackwardCondition


## Supported Types

### WorkflowExpressionConditionModelInput

```go
workflowEdgeModelInputBackwardCondition := components.CreateWorkflowEdgeModelInputBackwardConditionExpression(components.WorkflowExpressionConditionModelInput{/* values here */})
```

### WorkflowLLMConditionModelInput

```go
workflowEdgeModelInputBackwardCondition := components.CreateWorkflowEdgeModelInputBackwardConditionLlm(components.WorkflowLLMConditionModelInput{/* values here */})
```

### WorkflowResultConditionModelInput

```go
workflowEdgeModelInputBackwardCondition := components.CreateWorkflowEdgeModelInputBackwardConditionResult(components.WorkflowResultConditionModelInput{/* values here */})
```

### WorkflowUnconditionalModelInput

```go
workflowEdgeModelInputBackwardCondition := components.CreateWorkflowEdgeModelInputBackwardConditionUnconditional(components.WorkflowUnconditionalModelInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowEdgeModelInputBackwardCondition.Type {
	case components.WorkflowEdgeModelInputBackwardConditionTypeExpression:
		// workflowEdgeModelInputBackwardCondition.WorkflowExpressionConditionModelInput is populated
	case components.WorkflowEdgeModelInputBackwardConditionTypeLlm:
		// workflowEdgeModelInputBackwardCondition.WorkflowLLMConditionModelInput is populated
	case components.WorkflowEdgeModelInputBackwardConditionTypeResult:
		// workflowEdgeModelInputBackwardCondition.WorkflowResultConditionModelInput is populated
	case components.WorkflowEdgeModelInputBackwardConditionTypeUnconditional:
		// workflowEdgeModelInputBackwardCondition.WorkflowUnconditionalModelInput is populated
}
```
