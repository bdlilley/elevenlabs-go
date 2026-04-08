# ASTLLMNodeInput


## Supported Types

### ASTLLMNode1

```go
astllmNodeInput := components.CreateASTLLMNodeInputASTLLMNode1(components.ASTLLMNode1{/* values here */})
```

### ASTLLMNode2

```go
astllmNodeInput := components.CreateASTLLMNodeInputASTLLMNode2(components.ASTLLMNode2{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch astllmNodeInput.Type {
	case components.ASTLLMNodeInputTypeASTLLMNode1:
		// astllmNodeInput.ASTLLMNode1 is populated
	case components.ASTLLMNodeInputTypeASTLLMNode2:
		// astllmNodeInput.ASTLLMNode2 is populated
}
```
