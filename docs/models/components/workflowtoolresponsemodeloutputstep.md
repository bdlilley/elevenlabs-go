# WorkflowToolResponseModelOutputStep


## Supported Types

### WorkflowToolEdgeStepModel

```go
workflowToolResponseModelOutputStep := components.CreateWorkflowToolResponseModelOutputStepEdge(components.WorkflowToolEdgeStepModel{/* values here */})
```

### WorkflowToolMaxIterationsExceededStepModel

```go
workflowToolResponseModelOutputStep := components.CreateWorkflowToolResponseModelOutputStepMaxIterationsExceeded(components.WorkflowToolMaxIterationsExceededStepModel{/* values here */})
```

### WorkflowToolNestedToolsStepModelOutput

```go
workflowToolResponseModelOutputStep := components.CreateWorkflowToolResponseModelOutputStepNestedTools(components.WorkflowToolNestedToolsStepModelOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch workflowToolResponseModelOutputStep.Type {
	case components.WorkflowToolResponseModelOutputStepTypeEdge:
		// workflowToolResponseModelOutputStep.WorkflowToolEdgeStepModel is populated
	case components.WorkflowToolResponseModelOutputStepTypeMaxIterationsExceeded:
		// workflowToolResponseModelOutputStep.WorkflowToolMaxIterationsExceededStepModel is populated
	case components.WorkflowToolResponseModelOutputStepTypeNestedTools:
		// workflowToolResponseModelOutputStep.WorkflowToolNestedToolsStepModelOutput is populated
}
```
