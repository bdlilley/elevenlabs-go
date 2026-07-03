# MCPToolConfigOverrideInputInputOverrides


## Supported Types

### ConstantSchemaOverride

```go
mcpToolConfigOverrideInputInputOverrides := components.CreateMCPToolConfigOverrideInputInputOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
mcpToolConfigOverrideInputInputOverrides := components.CreateMCPToolConfigOverrideInputInputOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
mcpToolConfigOverrideInputInputOverrides := components.CreateMCPToolConfigOverrideInputInputOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

### OmitSchemaOverride

```go
mcpToolConfigOverrideInputInputOverrides := components.CreateMCPToolConfigOverrideInputInputOverridesOmit(components.OmitSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpToolConfigOverrideInputInputOverrides.Type {
	case components.MCPToolConfigOverrideInputInputOverridesTypeConstant:
		// mcpToolConfigOverrideInputInputOverrides.ConstantSchemaOverride is populated
	case components.MCPToolConfigOverrideInputInputOverridesTypeDynamicVariable:
		// mcpToolConfigOverrideInputInputOverrides.DynamicVariableSchemaOverride is populated
	case components.MCPToolConfigOverrideInputInputOverridesTypeLlm:
		// mcpToolConfigOverrideInputInputOverrides.LLMSchemaOverride is populated
	case components.MCPToolConfigOverrideInputInputOverridesTypeOmit:
		// mcpToolConfigOverrideInputInputOverrides.OmitSchemaOverride is populated
}
```
