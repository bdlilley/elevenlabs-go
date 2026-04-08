# WorkflowToolResponseModelInputStep


## Supported Types

### WorkflowToolEdgeStepModel

```go
workflowToolResponseModelInputStep := components.CreateWorkflowToolResponseModelInputStepEdge(components.WorkflowToolEdgeStepModel{/* values here */})
```

### WorkflowToolMaxIterationsExceededStepModel

```go
workflowToolResponseModelInputStep := components.CreateWorkflowToolResponseModelInputStepMaxIterationsExceeded(components.WorkflowToolMaxIterationsExceededStepModel{/* values here */})
```

### WorkflowToolNestedToolsStepModelInput

```go
workflowToolResponseModelInputStep := components.CreateWorkflowToolResponseModelInputStepNestedTools(components.WorkflowToolNestedToolsStepModelInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowToolResponseModelInputStep.Type {
	case components.WorkflowToolResponseModelInputStepTypeEdge:
		// workflowToolResponseModelInputStep.WorkflowToolEdgeStepModel is populated
	case components.WorkflowToolResponseModelInputStepTypeMaxIterationsExceeded:
		// workflowToolResponseModelInputStep.WorkflowToolMaxIterationsExceededStepModel is populated
	case components.WorkflowToolResponseModelInputStepTypeNestedTools:
		// workflowToolResponseModelInputStep.WorkflowToolNestedToolsStepModelInput is populated
}
```
