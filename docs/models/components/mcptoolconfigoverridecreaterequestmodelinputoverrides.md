# MCPToolConfigOverrideCreateRequestModelInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigOverrideCreateRequestModelInputOverrides := components.CreateMCPToolConfigOverrideCreateRequestModelInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigOverrideCreateRequestModelInputOverrides := components.CreateMCPToolConfigOverrideCreateRequestModelInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigOverrideCreateRequestModelInputOverrides := components.CreateMCPToolConfigOverrideCreateRequestModelInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigOverrideCreateRequestModelInputOverrides.Type {
	case components.MCPToolConfigOverrideCreateRequestModelInputOverridesTypeConstant:
		// mcpToolConfigOverrideCreateRequestModelInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigOverrideCreateRequestModelInputOverridesTypeDynamicVariable:
		// mcpToolConfigOverrideCreateRequestModelInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigOverrideCreateRequestModelInputOverridesTypeLlm:
		// mcpToolConfigOverrideCreateRequestModelInputOverrides.LLMSchemaOverride is populated
}
```
