# MCPToolConfigOverrideInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigOverrideInputOverrides := components.CreateMCPToolConfigOverrideInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigOverrideInputOverrides := components.CreateMCPToolConfigOverrideInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigOverrideInputOverrides := components.CreateMCPToolConfigOverrideInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigOverrideInputOverrides.Type {
	case components.MCPToolConfigOverrideInputOverridesTypeConstant:
		// mcpToolConfigOverrideInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigOverrideInputOverridesTypeDynamicVariable:
		// mcpToolConfigOverrideInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigOverrideInputOverridesTypeLlm:
		// mcpToolConfigOverrideInputOverrides.LLMSchemaOverride is populated
	default:
		// Unknown type - use mcpToolConfigOverrideInputOverrides.GetUnknownRaw() for raw JSON
}
```
