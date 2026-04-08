# ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut

Successful Response


## Supported Types

### GetResponseUnitTestResponseModel

```go
responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut := operations.CreateResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutLlm(components.GetResponseUnitTestResponseModel{/* values here */})
```

### GetToolCallUnitTestResponseModel

```go
responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut := operations.CreateResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTool(components.GetToolCallUnitTestResponseModel{/* values here */})
```

### GetSimulationTestResponseModel

```go
responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut := operations.CreateResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutSimulation(components.GetSimulationTestResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.Type {
	case operations.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTypeLlm:
		// responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetResponseUnitTestResponseModel is populated
	case operations.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTypeTool:
		// responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetToolCallUnitTestResponseModel is populated
	case operations.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTypeSimulation:
		// responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetSimulationTestResponseModel is populated
	default:
		// Unknown type - use responseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetUnknownRaw() for raw JSON
}
```
