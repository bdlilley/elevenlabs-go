# WorkflowEdgeModelOutputForwardCondition


## Supported Types

### WorkflowExpressionConditionModelOutput

```go
workflowEdgeModelOutputForwardCondition := components.CreateWorkflowEdgeModelOutputForwardConditionExpression(components.WorkflowExpressionConditionModelOutput{/* values here */})
```

### WorkflowLLMConditionModelOutput

```go
workflowEdgeModelOutputForwardCondition := components.CreateWorkflowEdgeModelOutputForwardConditionLlm(components.WorkflowLLMConditionModelOutput{/* values here */})
```

### WorkflowResultConditionModelOutput

```go
workflowEdgeModelOutputForwardCondition := components.CreateWorkflowEdgeModelOutputForwardConditionResult(components.WorkflowResultConditionModelOutput{/* values here */})
```

### WorkflowUnconditionalModelOutput

```go
workflowEdgeModelOutputForwardCondition := components.CreateWorkflowEdgeModelOutputForwardConditionUnconditional(components.WorkflowUnconditionalModelOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowEdgeModelOutputForwardCondition.Type {
	case components.WorkflowEdgeModelOutputForwardConditionTypeExpression:
		// workflowEdgeModelOutputForwardCondition.WorkflowExpressionConditionModelOutput is populated
	case components.WorkflowEdgeModelOutputForwardConditionTypeLlm:
		// workflowEdgeModelOutputForwardCondition.WorkflowLLMConditionModelOutput is populated
	case components.WorkflowEdgeModelOutputForwardConditionTypeResult:
		// workflowEdgeModelOutputForwardCondition.WorkflowResultConditionModelOutput is populated
	case components.WorkflowEdgeModelOutputForwardConditionTypeUnconditional:
		// workflowEdgeModelOutputForwardCondition.WorkflowUnconditionalModelOutput is populated
}
```
