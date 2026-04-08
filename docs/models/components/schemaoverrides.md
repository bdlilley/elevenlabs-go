# SchemaOverrides


## Supported Types

### ConstantSchemaOverride

```go
schemaOverrides := components.CreateSchemaOverridesConstant(components.ConstantSchemaOverride{/* values here */})
```

### DynamicVariableSchemaOverride

```go
schemaOverrides := components.CreateSchemaOverridesDynamicVariable(components.DynamicVariableSchemaOverride{/* values here */})
```

### LLMSchemaOverride

```go
schemaOverrides := components.CreateSchemaOverridesLlm(components.LLMSchemaOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch schemaOverrides.Type {
	case components.SchemaOverridesTypeConstant:
		// schemaOverrides.ConstantSchemaOverride is populated
	case components.SchemaOverridesTypeDynamicVariable:
		// schemaOverrides.DynamicVariableSchemaOverride is populated
	case components.SchemaOverridesTypeLlm:
		// schemaOverrides.LLMSchemaOverride is populated
	default:
		// Unknown type - use schemaOverrides.GetUnknownRaw() for raw JSON
}
```
