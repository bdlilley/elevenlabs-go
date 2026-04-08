# MCPToolConfigInputInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigInputInputOverrides := components.CreateMCPToolConfigInputInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigInputInputOverrides := components.CreateMCPToolConfigInputInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigInputInputOverrides := components.CreateMCPToolConfigInputInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigInputInputOverrides.Type {
	case components.MCPToolConfigInputInputOverridesTypeConstant:
		// mcpToolConfigInputInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigInputInputOverridesTypeDynamicVariable:
		// mcpToolConfigInputInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigInputInputOverridesTypeLlm:
		// mcpToolConfigInputInputOverrides.LLMSchemaOverride is populated
}
```
