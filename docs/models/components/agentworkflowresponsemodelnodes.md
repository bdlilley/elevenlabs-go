# AgentWorkflowResponseModelNodes


## Supported Types

### WorkflowEndNodeModelOutput

```go
agentWorkflowResponseModelNodes := components.CreateAgentWorkflowResponseModelNodesEnd(components.WorkflowEndNodeModelOutput{/* values here */})
```

### WorkflowOverrideAgentNodeModelOutput

```go
agentWorkflowResponseModelNodes := components.CreateAgentWorkflowResponseModelNodesOverrideAgent(components.WorkflowOverrideAgentNodeModelOutput{/* values here */})
```

### WorkflowPhoneNumberNodeModelOutput

```go
agentWorkflowResponseModelNodes := components.CreateAgentWorkflowResponseModelNodesPhoneNumber(components.WorkflowPhoneNumberNodeModelOutput{/* values here */})
```

### WorkflowStandaloneAgentNodeModelOutput

```go
agentWorkflowResponseModelNodes := components.CreateAgentWorkflowResponseModelNodesStandaloneAgent(components.WorkflowStandaloneAgentNodeModelOutput{/* values here */})
```

### WorkflowStartNodeModelOutput

```go
agentWorkflowResponseModelNodes := components.CreateAgentWorkflowResponseModelNodesStart(components.WorkflowStartNodeModelOutput{/* values here */})
```

### WorkflowToolNodeModelOutput

```go
agentWorkflowResponseModelNodes := components.CreateAgentWorkflowResponseModelNodesTool(components.WorkflowToolNodeModelOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch agentWorkflowResponseModelNodes.Type {
	case components.AgentWorkflowResponseModelNodesTypeEnd:
		// agentWorkflowResponseModelNodes.WorkflowEndNodeModelOutput is populated
	case components.AgentWorkflowResponseModelNodesTypeOverrideAgent:
		// agentWorkflowResponseModelNodes.WorkflowOverrideAgentNodeModelOutput is populated
	case components.AgentWorkflowResponseModelNodesTypePhoneNumber:
		// agentWorkflowResponseModelNodes.WorkflowPhoneNumberNodeModelOutput is populated
	case components.AgentWorkflowResponseModelNodesTypeStandaloneAgent:
		// agentWorkflowResponseModelNodes.WorkflowStandaloneAgentNodeModelOutput is populated
	case components.AgentWorkflowResponseModelNodesTypeStart:
		// agentWorkflowResponseModelNodes.WorkflowStartNodeModelOutput is populated
	case components.AgentWorkflowResponseModelNodesTypeTool:
		// agentWorkflowResponseModelNodes.WorkflowToolNodeModelOutput is populated
}
```
