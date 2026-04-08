# ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGet

Successful Response


## Supported Types

### GetResponseUnitTestResponseModel

```go
responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet := operations.CreateResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetLlm(components.GetResponseUnitTestResponseModel{/* values here */})
```

### GetToolCallUnitTestResponseModel

```go
responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet := operations.CreateResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTool(components.GetToolCallUnitTestResponseModel{/* values here */})
```

### GetSimulationTestResponseModel

```go
responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet := operations.CreateResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetSimulation(components.GetSimulationTestResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet.Type {
	case operations.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTypeLlm:
		// responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet.GetResponseUnitTestResponseModel is populated
	case operations.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTypeTool:
		// responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet.GetToolCallUnitTestResponseModel is populated
	case operations.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTypeSimulation:
		// responseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet.GetSimulationTestResponseModel is populated
}
```
