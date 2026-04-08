# UpdateAgentResponseTestRouteTestRequest

Agent test to update


## Supported Types

### UpdateResponseUnitTestRequest

```go
updateAgentResponseTestRouteTestRequest := operations.CreateUpdateAgentResponseTestRouteTestRequestUpdateResponseUnitTestRequest(components.UpdateResponseUnitTestRequest{/* values here */})
```

### UpdateToolCallUnitTestRequest

```go
updateAgentResponseTestRouteTestRequest := operations.CreateUpdateAgentResponseTestRouteTestRequestUpdateToolCallUnitTestRequest(components.UpdateToolCallUnitTestRequest{/* values here */})
```

### UpdateSimulationTestRequest

```go
updateAgentResponseTestRouteTestRequest := operations.CreateUpdateAgentResponseTestRouteTestRequestUpdateSimulationTestRequest(components.UpdateSimulationTestRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch updateAgentResponseTestRouteTestRequest.Type {
	case operations.UpdateAgentResponseTestRouteTestRequestTypeUpdateResponseUnitTestRequest:
		// updateAgentResponseTestRouteTestRequest.UpdateResponseUnitTestRequest is populated
	case operations.UpdateAgentResponseTestRouteTestRequestTypeUpdateToolCallUnitTestRequest:
		// updateAgentResponseTestRouteTestRequest.UpdateToolCallUnitTestRequest is populated
	case operations.UpdateAgentResponseTestRouteTestRequestTypeUpdateSimulationTestRequest:
		// updateAgentResponseTestRouteTestRequest.UpdateSimulationTestRequest is populated
}
```
