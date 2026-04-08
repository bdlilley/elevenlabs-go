# ArrayJSONSchemaPropertyOutputItems


## Supported Types

### LiteralJSONSchemaProperty

```go
arrayJSONSchemaPropertyOutputItems := components.CreateArrayJSONSchemaPropertyOutputItemsLiteralJSONSchemaProperty(components.LiteralJSONSchemaProperty{/* values here */})
```

### ObjectJSONSchemaPropertyOutput

```go
arrayJSONSchemaPropertyOutputItems := components.CreateArrayJSONSchemaPropertyOutputItemsObjectJSONSchemaPropertyOutput(components.ObjectJSONSchemaPropertyOutput{/* values here */})
```

### ArrayJSONSchemaPropertyOutput

```go
arrayJSONSchemaPropertyOutputItems := components.CreateArrayJSONSchemaPropertyOutputItemsArrayJSONSchemaPropertyOutput(components.ArrayJSONSchemaPropertyOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch arrayJSONSchemaPropertyOutputItems.Type {
	case components.ArrayJSONSchemaPropertyOutputItemsTypeLiteralJSONSchemaProperty:
		// arrayJSONSchemaPropertyOutputItems.LiteralJSONSchemaProperty is populated
	case components.ArrayJSONSchemaPropertyOutputItemsTypeObjectJSONSchemaPropertyOutput:
		// arrayJSONSchemaPropertyOutputItems.ObjectJSONSchemaPropertyOutput is populated
	case components.ArrayJSONSchemaPropertyOutputItemsTypeArrayJSONSchemaPropertyOutput:
		// arrayJSONSchemaPropertyOutputItems.ArrayJSONSchemaPropertyOutput is populated
}
```
