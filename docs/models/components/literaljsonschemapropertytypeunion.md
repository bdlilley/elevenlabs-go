# LiteralJSONSchemaPropertyTypeUnion


## Supported Types

### LiteralJSONSchemaPropertyTypeEnum

```go
literalJSONSchemaPropertyTypeUnion := components.CreateLiteralJSONSchemaPropertyTypeUnionLiteralJSONSchemaPropertyTypeEnum(components.LiteralJSONSchemaPropertyTypeEnum{/* values here */})
```

### 

```go
literalJSONSchemaPropertyTypeUnion := components.CreateLiteralJSONSchemaPropertyTypeUnionArrayOfStr([]string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch literalJSONSchemaPropertyTypeUnion.Type {
	case components.LiteralJSONSchemaPropertyTypeUnionTypeLiteralJSONSchemaPropertyTypeEnum:
		// literalJSONSchemaPropertyTypeUnion.LiteralJSONSchemaPropertyTypeEnum is populated
	case components.LiteralJSONSchemaPropertyTypeUnionTypeArrayOfStr:
		// literalJSONSchemaPropertyTypeUnion.ArrayOfStr is populated
}
```
