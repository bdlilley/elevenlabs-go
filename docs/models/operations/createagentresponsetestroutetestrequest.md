# CreateAgentResponseTestRouteTestRequest

Create Chat Response Test Request Information


## Supported Types

### CreateResponseUnitTestRequest

```go
createAgentResponseTestRouteTestRequest := operations.CreateCreateAgentResponseTestRouteTestRequestCreateResponseUnitTestRequest(components.CreateResponseUnitTestRequest{/* values here */})
```

### CreateToolCallUnitTestRequest

```go
createAgentResponseTestRouteTestRequest := operations.CreateCreateAgentResponseTestRouteTestRequestCreateToolCallUnitTestRequest(components.CreateToolCallUnitTestRequest{/* values here */})
```

### CreateSimulationTestRequest

```go
createAgentResponseTestRouteTestRequest := operations.CreateCreateAgentResponseTestRouteTestRequestCreateSimulationTestRequest(components.CreateSimulationTestRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch createAgentResponseTestRouteTestRequest.Type {
	case operations.CreateAgentResponseTestRouteTestRequestTypeCreateResponseUnitTestRequest:
		// createAgentResponseTestRouteTestRequest.CreateResponseUnitTestRequest is populated
	case operations.CreateAgentResponseTestRouteTestRequestTypeCreateToolCallUnitTestRequest:
		// createAgentResponseTestRouteTestRequest.CreateToolCallUnitTestRequest is populated
	case operations.CreateAgentResponseTestRouteTestRequestTypeCreateSimulationTestRequest:
		// createAgentResponseTestRouteTestRequest.CreateSimulationTestRequest is populated
}
```
