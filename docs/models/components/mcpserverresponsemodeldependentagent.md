# MCPServerResponseModelDependentAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
mcpServerResponseModelDependentAgent := components.CreateMCPServerResponseModelDependentAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
mcpServerResponseModelDependentAgent := components.CreateMCPServerResponseModelDependentAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerResponseModelDependentAgent.Type {
	case components.MCPServerResponseModelDependentAgentTypeAvailable:
		// mcpServerResponseModelDependentAgent.DependentAvailableAgentIdentifier is populated
	case components.MCPServerResponseModelDependentAgentTypeUnknown:
		// mcpServerResponseModelDependentAgent.DependentUnknownAgentIdentifier is populated
}
```
