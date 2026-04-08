# MCPToolConfigOverrideUpdateRequestModelInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigOverrideUpdateRequestModelInputOverrides := components.CreateMCPToolConfigOverrideUpdateRequestModelInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigOverrideUpdateRequestModelInputOverrides := components.CreateMCPToolConfigOverrideUpdateRequestModelInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigOverrideUpdateRequestModelInputOverrides := components.CreateMCPToolConfigOverrideUpdateRequestModelInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigOverrideUpdateRequestModelInputOverrides.Type {
	case components.MCPToolConfigOverrideUpdateRequestModelInputOverridesTypeConstant:
		// mcpToolConfigOverrideUpdateRequestModelInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigOverrideUpdateRequestModelInputOverridesTypeDynamicVariable:
		// mcpToolConfigOverrideUpdateRequestModelInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigOverrideUpdateRequestModelInputOverridesTypeLlm:
		// mcpToolConfigOverrideUpdateRequestModelInputOverrides.LLMSchemaOverride is populated
}
```
