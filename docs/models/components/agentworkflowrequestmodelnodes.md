# AgentWorkflowRequestModelNodes


## Supported Types

### WorkflowEndNodeModelInput

```go
agentWorkflowRequestModelNodes := components.CreateAgentWorkflowRequestModelNodesEnd(components.WorkflowEndNodeModelInput{/* values here */})
```

### WorkflowOverrideAgentNodeModelInput

```go
agentWorkflowRequestModelNodes := components.CreateAgentWorkflowRequestModelNodesOverrideAgent(components.WorkflowOverrideAgentNodeModelInput{/* values here */})
```

### WorkflowPhoneNumberNodeModelInput

```go
agentWorkflowRequestModelNodes := components.CreateAgentWorkflowRequestModelNodesPhoneNumber(components.WorkflowPhoneNumberNodeModelInput{/* values here */})
```

### WorkflowStandaloneAgentNodeModelInput

```go
agentWorkflowRequestModelNodes := components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(components.WorkflowStandaloneAgentNodeModelInput{/* values here */})
```

### WorkflowStartNodeModelInput

```go
agentWorkflowRequestModelNodes := components.CreateAgentWorkflowRequestModelNodesStart(components.WorkflowStartNodeModelInput{/* values here */})
```

### WorkflowToolNodeModelInput

```go
agentWorkflowRequestModelNodes := components.CreateAgentWorkflowRequestModelNodesTool(components.WorkflowToolNodeModelInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch agentWorkflowRequestModelNodes.Type {
	case components.AgentWorkflowRequestModelNodesTypeEnd:
		// agentWorkflowRequestModelNodes.WorkflowEndNodeModelInput is populated
	case components.AgentWorkflowRequestModelNodesTypeOverrideAgent:
		// agentWorkflowRequestModelNodes.WorkflowOverrideAgentNodeModelInput is populated
	case components.AgentWorkflowRequestModelNodesTypePhoneNumber:
		// agentWorkflowRequestModelNodes.WorkflowPhoneNumberNodeModelInput is populated
	case components.AgentWorkflowRequestModelNodesTypeStandaloneAgent:
		// agentWorkflowRequestModelNodes.WorkflowStandaloneAgentNodeModelInput is populated
	case components.AgentWorkflowRequestModelNodesTypeStart:
		// agentWorkflowRequestModelNodes.WorkflowStartNodeModelInput is populated
	case components.AgentWorkflowRequestModelNodesTypeTool:
		// agentWorkflowRequestModelNodes.WorkflowToolNodeModelInput is populated
}
```
