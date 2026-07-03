# MCPToolConfigOverrideOutputInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigOverrideOutputInputOverrides := components.CreateMCPToolConfigOverrideOutputInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigOverrideOutputInputOverrides := components.CreateMCPToolConfigOverrideOutputInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigOverrideOutputInputOverrides := components.CreateMCPToolConfigOverrideOutputInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

### OmitSchemaOverride

```go
mcpToolConfigOverrideOutputInputOverrides := components.CreateMCPToolConfigOverrideOutputInputOverridesOmit(components.OmitSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigOverrideOutputInputOverrides.Type {
	case components.MCPToolConfigOverrideOutputInputOverridesTypeConstant:
		// mcpToolConfigOverrideOutputInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigOverrideOutputInputOverridesTypeDynamicVariable:
		// mcpToolConfigOverrideOutputInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigOverrideOutputInputOverridesTypeLlm:
		// mcpToolConfigOverrideOutputInputOverrides.LLMSchemaOverride is populated
	case components.MCPToolConfigOverrideOutputInputOverridesTypeOmit:
		// mcpToolConfigOverrideOutputInputOverrides.OmitSchemaOverride is populated
}
```
