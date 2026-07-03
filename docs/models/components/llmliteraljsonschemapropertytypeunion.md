# LLMLiteralJSONSchemaPropertyTypeUnion


## Supported Types

### LLMLiteralJSONSchemaPropertyTypeEnum

```go
llmLiteralJSONSchemaPropertyTypeUnion := components.CreateLLMLiteralJSONSchemaPropertyTypeUnionLLMLiteralJSONSchemaPropertyTypeEnum(components.LLMLiteralJSONSchemaPropertyTypeEnum{/* values here */})
```

### 

```go
llmLiteralJSONSchemaPropertyTypeUnion := components.CreateLLMLiteralJSONSchemaPropertyTypeUnionArrayOfStr([]string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch llmLiteralJSONSchemaPropertyTypeUnion.Type {
	case components.LLMLiteralJSONSchemaPropertyTypeUnionTypeLLMLiteralJSONSchemaPropertyTypeEnum:
		// llmLiteralJSONSchemaPropertyTypeUnion.LLMLiteralJSONSchemaPropertyTypeEnum is populated
	case components.LLMLiteralJSONSchemaPropertyTypeUnionTypeArrayOfStr:
		// llmLiteralJSONSchemaPropertyTypeUnion.ArrayOfStr is populated
}
```
