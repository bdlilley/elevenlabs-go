# GetKnowledgeBaseSummaryTextResponseModelDependentAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
getKnowledgeBaseSummaryTextResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryTextResponseModelDependentAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
getKnowledgeBaseSummaryTextResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryTextResponseModelDependentAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getKnowledgeBaseSummaryTextResponseModelDependentAgent.Type {
	case components.GetKnowledgeBaseSummaryTextResponseModelDependentAgentTypeAvailable:
		// getKnowledgeBaseSummaryTextResponseModelDependentAgent.DependentAvailableAgentIdentifier is populated
	case components.GetKnowledgeBaseSummaryTextResponseModelDependentAgentTypeUnknown:
		// getKnowledgeBaseSummaryTextResponseModelDependentAgent.DependentUnknownAgentIdentifier is populated
	default:
		// Unknown type - use getKnowledgeBaseSummaryTextResponseModelDependentAgent.GetUnknownRaw() for raw JSON
}
```
