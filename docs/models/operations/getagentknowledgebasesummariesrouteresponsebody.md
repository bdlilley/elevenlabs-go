# GetAgentKnowledgeBaseSummariesRouteResponseBody


## Supported Types

### KnowledgeBaseSummaryBatchSuccessfulResponseModel

```go
getAgentKnowledgeBaseSummariesRouteResponseBody := operations.CreateGetAgentKnowledgeBaseSummariesRouteResponseBodySuccess(components.KnowledgeBaseSummaryBatchSuccessfulResponseModel{/* values here */})
```

### BatchFailureResponseModel

```go
getAgentKnowledgeBaseSummariesRouteResponseBody := operations.CreateGetAgentKnowledgeBaseSummariesRouteResponseBodyFailure(components.BatchFailureResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getAgentKnowledgeBaseSummariesRouteResponseBody.Type {
	case operations.GetAgentKnowledgeBaseSummariesRouteResponseBodyTypeSuccess:
		// getAgentKnowledgeBaseSummariesRouteResponseBody.KnowledgeBaseSummaryBatchSuccessfulResponseModel is populated
	case operations.GetAgentKnowledgeBaseSummariesRouteResponseBodyTypeFailure:
		// getAgentKnowledgeBaseSummariesRouteResponseBody.BatchFailureResponseModel is populated
}
```
