# GetKnowledgeBaseSummaryFolderResponseModelDependentAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
getKnowledgeBaseSummaryFolderResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryFolderResponseModelDependentAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
getKnowledgeBaseSummaryFolderResponseModelDependentAgent := components.CreateGetKnowledgeBaseSummaryFolderResponseModelDependentAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getKnowledgeBaseSummaryFolderResponseModelDependentAgent.Type {
	case components.GetKnowledgeBaseSummaryFolderResponseModelDependentAgentTypeAvailable:
		// getKnowledgeBaseSummaryFolderResponseModelDependentAgent.DependentAvailableAgentIdentifier is populated
	case components.GetKnowledgeBaseSummaryFolderResponseModelDependentAgentTypeUnknown:
		// getKnowledgeBaseSummaryFolderResponseModelDependentAgent.DependentUnknownAgentIdentifier is populated
}
```
