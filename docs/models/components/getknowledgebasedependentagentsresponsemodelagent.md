# GetKnowledgeBaseDependentAgentsResponseModelAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
getKnowledgeBaseDependentAgentsResponseModelAgent := components.CreateGetKnowledgeBaseDependentAgentsResponseModelAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
getKnowledgeBaseDependentAgentsResponseModelAgent := components.CreateGetKnowledgeBaseDependentAgentsResponseModelAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getKnowledgeBaseDependentAgentsResponseModelAgent.Type {
	case components.GetKnowledgeBaseDependentAgentsResponseModelAgentTypeAvailable:
		// getKnowledgeBaseDependentAgentsResponseModelAgent.DependentAvailableAgentIdentifier is populated
	case components.GetKnowledgeBaseDependentAgentsResponseModelAgentTypeUnknown:
		// getKnowledgeBaseDependentAgentsResponseModelAgent.DependentUnknownAgentIdentifier is populated
	default:
		// Unknown type - use getKnowledgeBaseDependentAgentsResponseModelAgent.GetUnknownRaw() for raw JSON
}
```
