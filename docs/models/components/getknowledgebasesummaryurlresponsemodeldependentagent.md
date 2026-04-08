# GetKnowledgeBaseSummaryURLResponseModelDependentAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
getKnowledgeBaseSummaryURLResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryURLResponseModelDependentAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
getKnowledgeBaseSummaryURLResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryURLResponseModelDependentAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getKnowledgeBaseSummaryURLResponseModelDependentAgent.Type {
	case components.GetKnowledgeBaseSummaryURLResponseModelDependentAgentTypeAvailable:
		// getKnowledgeBaseSummaryURLResponseModelDependentAgent.DependentAvailableAgentIdentifier is populated
	case components.GetKnowledgeBaseSummaryURLResponseModelDependentAgentTypeUnknown:
		// getKnowledgeBaseSummaryURLResponseModelDependentAgent.DependentUnknownAgentIdentifier is populated
}
```
