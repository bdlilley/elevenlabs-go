# GetKnowledgeBaseSummaryFileResponseModelDependentAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
getKnowledgeBaseSummaryFileResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryFileResponseModelDependentAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
getKnowledgeBaseSummaryFileResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryFileResponseModelDependentAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getKnowledgeBaseSummaryFileResponseModelDependentAgent.Type {
	case components.GetKnowledgeBaseSummaryFileResponseModelDependentAgentTypeAvailable:
		// getKnowledgeBaseSummaryFileResponseModelDependentAgent.DependentAvailableAgentIdentifier is populated
	case components.GetKnowledgeBaseSummaryFileResponseModelDependentAgentTypeUnknown:
		// getKnowledgeBaseSummaryFileResponseModelDependentAgent.DependentUnknownAgentIdentifier is populated
	default:
		// Unknown type - use getKnowledgeBaseSummaryFileResponseModelDependentAgent.GetUnknownRaw() for raw JSON
}
```
