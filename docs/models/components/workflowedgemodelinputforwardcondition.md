# WorkflowEdgeModelInputForwardCondition


## Supported Types

### WorkflowExpressionConditionModelInput

```go
workflowEdgeModelInputForwardCondition := components.CreateWorkflowEdgeModelInputForwardConditionExpression(components.WorkflowExpressionConditionModelInput{/* values here */})
```

### WorkflowLLMConditionModelInput

```go
workflowEdgeModelInputForwardCondition := components.CreateWorkflowEdgeModelInputForwardConditionLlm(components.WorkflowLLMConditionModelInput{/* values here */})
```

### WorkflowResultConditionModelInput

```go
workflowEdgeModelInputForwardCondition := components.CreateWorkflowEdgeModelInputForwardConditionResult(components.WorkflowResultConditionModelInput{/* values here */})
```

### WorkflowUnconditionalModelInput

```go
workflowEdgeModelInputForwardCondition := components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(components.WorkflowUnconditionalModelInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowEdgeModelInputForwardCondition.Type {
	case components.WorkflowEdgeModelInputForwardConditionTypeExpression:
		// workflowEdgeModelInputForwardCondition.WorkflowExpressionConditionModelInput is populated
	case components.WorkflowEdgeModelInputForwardConditionTypeLlm:
		// workflowEdgeModelInputForwardCondition.WorkflowLLMConditionModelInput is populated
	case components.WorkflowEdgeModelInputForwardConditionTypeResult:
		// workflowEdgeModelInputForwardCondition.WorkflowResultConditionModelInput is populated
	case components.WorkflowEdgeModelInputForwardConditionTypeUnconditional:
		// workflowEdgeModelInputForwardCondition.WorkflowUnconditionalModelInput is populated
}
```
