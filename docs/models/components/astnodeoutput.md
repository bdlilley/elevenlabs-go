# ASTNodeOutput


## Supported Types

### ASTAdditionOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputAddOperator(components.ASTAdditionOperatorNodeOutput1{/* values here */})
```

### ASTAndOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputAndOperator(components.ASTAndOperatorNodeOutput1{/* values here */})
```

### ASTBooleanNodeOutput

```go
astNodeOutput := components.CreateASTNodeOutputBooleanLiteral(components.ASTBooleanNodeOutput{/* values here */})
```

### ASTConditionalOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputConditionalOperator(components.ASTConditionalOperatorNodeOutput1{/* values here */})
```

### ASTDivisionOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputDivOperator(components.ASTDivisionOperatorNodeOutput1{/* values here */})
```

### ASTDynamicVariableNodeOutput

```go
astNodeOutput := components.CreateASTNodeOutputDynamicVariable(components.ASTDynamicVariableNodeOutput{/* values here */})
```

### ASTEqualsOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputEqOperator(components.ASTEqualsOperatorNodeOutput1{/* values here */})
```

### ASTGreaterThanOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputGtOperator(components.ASTGreaterThanOperatorNodeOutput1{/* values here */})
```

### ASTGreaterThanOrEqualsOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputGteOperator(components.ASTGreaterThanOrEqualsOperatorNodeOutput1{/* values here */})
```

### ASTLLMNodeOutput

```go
astNodeOutput := components.CreateASTNodeOutputLlm(components.ASTLLMNodeOutput{/* values here */})
```

### ASTLessThanOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputLtOperator(components.ASTLessThanOperatorNodeOutput1{/* values here */})
```

### ASTLessThanOrEqualsOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputLteOperator(components.ASTLessThanOrEqualsOperatorNodeOutput1{/* values here */})
```

### ASTMultiplicationOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputMulOperator(components.ASTMultiplicationOperatorNodeOutput1{/* values here */})
```

### ASTNotEqualsOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputNeqOperator(components.ASTNotEqualsOperatorNodeOutput1{/* values here */})
```

### ASTNumberNodeOutput

```go
astNodeOutput := components.CreateASTNodeOutputNumberLiteral(components.ASTNumberNodeOutput{/* values here */})
```

### ASTOrOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputOrOperator(components.ASTOrOperatorNodeOutput1{/* values here */})
```

### ASTStringNodeOutput

```go
astNodeOutput := components.CreateASTNodeOutputStringLiteral(components.ASTStringNodeOutput{/* values here */})
```

### ASTSubtractionOperatorNodeOutput1

```go
astNodeOutput := components.CreateASTNodeOutputSubOperator(components.ASTSubtractionOperatorNodeOutput1{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch astNodeOutput.Type {
	case components.ASTNodeOutputTypeAddOperator:
		// astNodeOutput.ASTAdditionOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeAndOperator:
		// astNodeOutput.ASTAndOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeBooleanLiteral:
		// astNodeOutput.ASTBooleanNodeOutput is populated
	case components.ASTNodeOutputTypeConditionalOperator:
		// astNodeOutput.ASTConditionalOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeDivOperator:
		// astNodeOutput.ASTDivisionOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeDynamicVariable:
		// astNodeOutput.ASTDynamicVariableNodeOutput is populated
	case components.ASTNodeOutputTypeEqOperator:
		// astNodeOutput.ASTEqualsOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeGtOperator:
		// astNodeOutput.ASTGreaterThanOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeGteOperator:
		// astNodeOutput.ASTGreaterThanOrEqualsOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeLlm:
		// astNodeOutput.ASTLLMNodeOutput is populated
	case components.ASTNodeOutputTypeLtOperator:
		// astNodeOutput.ASTLessThanOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeLteOperator:
		// astNodeOutput.ASTLessThanOrEqualsOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeMulOperator:
		// astNodeOutput.ASTMultiplicationOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeNeqOperator:
		// astNodeOutput.ASTNotEqualsOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeNumberLiteral:
		// astNodeOutput.ASTNumberNodeOutput is populated
	case components.ASTNodeOutputTypeOrOperator:
		// astNodeOutput.ASTOrOperatorNodeOutput1 is populated
	case components.ASTNodeOutputTypeStringLiteral:
		// astNodeOutput.ASTStringNodeOutput is populated
	case components.ASTNodeOutputTypeSubOperator:
		// astNodeOutput.ASTSubtractionOperatorNodeOutput1 is populated
	default:
		// Unknown type - use astNodeOutput.GetUnknownRaw() for raw JSON
}
```
