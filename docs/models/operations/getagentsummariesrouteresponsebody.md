# GetAgentSummariesRouteResponseBody


## Supported Types

### AgentSummaryBatchSuccessfulResponseModel

```go
getAgentSummariesRouteResponseBody := operations.CreateGetAgentSummariesRouteResponseBodySuccess(components.AgentSummaryBatchSuccessfulResponseModel{/* values here */})
```

### BatchFailureResponseModel

```go
getAgentSummariesRouteResponseBody := operations.CreateGetAgentSummariesRouteResponseBodyFailure(components.BatchFailureResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getAgentSummariesRouteResponseBody.Type {
	case operations.GetAgentSummariesRouteResponseBodyTypeSuccess:
		// getAgentSummariesRouteResponseBody.AgentSummaryBatchSuccessfulResponseModel is populated
	case operations.GetAgentSummariesRouteResponseBodyTypeFailure:
		// getAgentSummariesRouteResponseBody.BatchFailureResponseModel is populated
	default:
		// Unknown type - use getAgentSummariesRouteResponseBody.GetUnknownRaw() for raw JSON
}
```
