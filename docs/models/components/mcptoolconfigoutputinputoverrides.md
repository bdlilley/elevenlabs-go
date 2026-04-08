# MCPToolConfigOutputInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigOutputInputOverrides := components.CreateMCPToolConfigOutputInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigOutputInputOverrides := components.CreateMCPToolConfigOutputInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigOutputInputOverrides := components.CreateMCPToolConfigOutputInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigOutputInputOverrides.Type {
	case components.MCPToolConfigOutputInputOverridesTypeConstant:
		// mcpToolConfigOutputInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigOutputInputOverridesTypeDynamicVariable:
		// mcpToolConfigOutputInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigOutputInputOverridesTypeLlm:
		// mcpToolConfigOutputInputOverrides.LLMSchemaOverride is populated
	default:
		// Unknown type - use mcpToolConfigOutputInputOverrides.GetUnknownRaw() for raw JSON
}
```
