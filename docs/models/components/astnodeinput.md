# ASTNodeInput


## Supported Types

### ASTAdditionOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputAddOperator(components.ASTAdditionOperatorNodeInput1{/* values here */})
```

### ASTAndOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputAndOperator(components.ASTAndOperatorNodeInput1{/* values here */})
```

### ASTBooleanNodeInput

```go
astNodeInput := components.CreateASTNodeInputBooleanLiteral(components.ASTBooleanNodeInput{/* values here */})
```

### ASTConditionalOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputConditionalOperator(components.ASTConditionalOperatorNodeInput1{/* values here */})
```

### ASTDivisionOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputDivOperator(components.ASTDivisionOperatorNodeInput1{/* values here */})
```

### ASTDynamicVariableNodeInput

```go
astNodeInput := components.CreateASTNodeInputDynamicVariable(components.ASTDynamicVariableNodeInput{/* values here */})
```

### ASTEqualsOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputEqOperator(components.ASTEqualsOperatorNodeInput1{/* values here */})
```

### ASTGreaterThanOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputGtOperator(components.ASTGreaterThanOperatorNodeInput1{/* values here */})
```

### ASTGreaterThanOrEqualsOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputGteOperator(components.ASTGreaterThanOrEqualsOperatorNodeInput1{/* values here */})
```

### ASTLLMNodeInput

```go
astNodeInput := components.CreateASTNodeInputLlm(components.ASTLLMNodeInput{/* values here */})
```

### ASTLessThanOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputLtOperator(components.ASTLessThanOperatorNodeInput1{/* values here */})
```

### ASTLessThanOrEqualsOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputLteOperator(components.ASTLessThanOrEqualsOperatorNodeInput1{/* values here */})
```

### ASTMultiplicationOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputMulOperator(components.ASTMultiplicationOperatorNodeInput1{/* values here */})
```

### ASTNotEqualsOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputNeqOperator(components.ASTNotEqualsOperatorNodeInput1{/* values here */})
```

### ASTNumberNodeInput

```go
astNodeInput := components.CreateASTNodeInputNumberLiteral(components.ASTNumberNodeInput{/* values here */})
```

### ASTOrOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputOrOperator(components.ASTOrOperatorNodeInput1{/* values here */})
```

### ASTStringNodeInput

```go
astNodeInput := components.CreateASTNodeInputStringLiteral(components.ASTStringNodeInput{/* values here */})
```

### ASTSubtractionOperatorNodeInput1

```go
astNodeInput := components.CreateASTNodeInputSubOperator(components.ASTSubtractionOperatorNodeInput1{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch astNodeInput.Type {
	case components.ASTNodeInputTypeAddOperator:
		// astNodeInput.ASTAdditionOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeAndOperator:
		// astNodeInput.ASTAndOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeBooleanLiteral:
		// astNodeInput.ASTBooleanNodeInput is populated
	case components.ASTNodeInputTypeConditionalOperator:
		// astNodeInput.ASTConditionalOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeDivOperator:
		// astNodeInput.ASTDivisionOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeDynamicVariable:
		// astNodeInput.ASTDynamicVariableNodeInput is populated
	case components.ASTNodeInputTypeEqOperator:
		// astNodeInput.ASTEqualsOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeGtOperator:
		// astNodeInput.ASTGreaterThanOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeGteOperator:
		// astNodeInput.ASTGreaterThanOrEqualsOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeLlm:
		// astNodeInput.ASTLLMNodeInput is populated
	case components.ASTNodeInputTypeLtOperator:
		// astNodeInput.ASTLessThanOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeLteOperator:
		// astNodeInput.ASTLessThanOrEqualsOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeMulOperator:
		// astNodeInput.ASTMultiplicationOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeNeqOperator:
		// astNodeInput.ASTNotEqualsOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeNumberLiteral:
		// astNodeInput.ASTNumberNodeInput is populated
	case components.ASTNodeInputTypeOrOperator:
		// astNodeInput.ASTOrOperatorNodeInput1 is populated
	case components.ASTNodeInputTypeStringLiteral:
		// astNodeInput.ASTStringNodeInput is populated
	case components.ASTNodeInputTypeSubOperator:
		// astNodeInput.ASTSubtractionOperatorNodeInput1 is populated
}
```
