# GetToolDependentAgentsResponseModelAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
getToolDependentAgentsResponseModelAgent := components.CreateGetToolDependentAgentsResponseModelAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
getToolDependentAgentsResponseModelAgent := components.CreateGetToolDependentAgentsResponseModelAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getToolDependentAgentsResponseModelAgent.Type {
	case components.GetToolDependentAgentsResponseModelAgentTypeAvailable:
		// getToolDependentAgentsResponseModelAgent.DependentAvailableAgentIdentifier is populated
	case components.GetToolDependentAgentsResponseModelAgentTypeUnknown:
		// getToolDependentAgentsResponseModelAgent.DependentUnknownAgentIdentifier is populated
}
```
