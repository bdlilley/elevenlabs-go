# WorkflowEdgeModelOutputBackwardCondition


## Supported Types

### WorkflowExpressionConditionModelOutput

```go
workflowEdgeModelOutputBackwardCondition := components.CreateWorkflowEdgeModelOutputBackwardConditionExpression(components.WorkflowExpressionConditionModelOutput{/* values here */})
```

### WorkflowLLMConditionModelOutput

```go
workflowEdgeModelOutputBackwardCondition := components.CreateWorkflowEdgeModelOutputBackwardConditionLlm(components.WorkflowLLMConditionModelOutput{/* values here */})
```

### WorkflowResultConditionModelOutput

```go
workflowEdgeModelOutputBackwardCondition := components.CreateWorkflowEdgeModelOutputBackwardConditionResult(components.WorkflowResultConditionModelOutput{/* values here */})
```

### WorkflowUnconditionalModelOutput

```go
workflowEdgeModelOutputBackwardCondition := components.CreateWorkflowEdgeModelOutputBackwardConditionUnconditional(components.WorkflowUnconditionalModelOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowEdgeModelOutputBackwardCondition.Type {
	case components.WorkflowEdgeModelOutputBackwardConditionTypeExpression:
		// workflowEdgeModelOutputBackwardCondition.WorkflowExpressionConditionModelOutput is populated
	case components.WorkflowEdgeModelOutputBackwardConditionTypeLlm:
		// workflowEdgeModelOutputBackwardCondition.WorkflowLLMConditionModelOutput is populated
	case components.WorkflowEdgeModelOutputBackwardConditionTypeResult:
		// workflowEdgeModelOutputBackwardCondition.WorkflowResultConditionModelOutput is populated
	case components.WorkflowEdgeModelOutputBackwardConditionTypeUnconditional:
		// workflowEdgeModelOutputBackwardCondition.WorkflowUnconditionalModelOutput is populated
	default:
		// Unknown type - use workflowEdgeModelOutputBackwardCondition.GetUnknownRaw() for raw JSON
}
```
