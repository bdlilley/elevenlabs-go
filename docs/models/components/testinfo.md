# TestInfo


## Supported Types

### ResponseUnitTestModel

```go
testInfo := components.CreateTestInfoLlm(components.ResponseUnitTestModel{/* values here */})
```

### SimulationTestModel

```go
testInfo := components.CreateTestInfoSimulation(components.SimulationTestModel{/* values here */})
```

### ToolCallUnitTestModel

```go
testInfo := components.CreateTestInfoTool(components.ToolCallUnitTestModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch testInfo.Type {
	case components.TestInfoTypeLlm:
		// testInfo.ResponseUnitTestModel is populated
	case components.TestInfoTypeSimulation:
		// testInfo.SimulationTestModel is populated
	case components.TestInfoTypeTool:
		// testInfo.ToolCallUnitTestModel is populated
	default:
		// Unknown type - use testInfo.GetUnknownRaw() for raw JSON
}
```
