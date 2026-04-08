# ArrayJSONSchemaPropertyInputItems


## Supported Types

### LiteralJSONSchemaProperty

```go
arrayJSONSchemaPropertyInputItems := components.CreateArrayJSONSchemaPropertyInputItemsLiteralJSONSchemaProperty(components.LiteralJSONSchemaProperty{/* values here */})
```

### ObjectJSONSchemaPropertyInput

```go
arrayJSONSchemaPropertyInputItems := components.CreateArrayJSONSchemaPropertyInputItemsObjectJSONSchemaPropertyInput(components.ObjectJSONSchemaPropertyInput{/* values here */})
```

### ArrayJSONSchemaPropertyInput

```go
arrayJSONSchemaPropertyInputItems := components.CreateArrayJSONSchemaPropertyInputItemsArrayJSONSchemaPropertyInput(components.ArrayJSONSchemaPropertyInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch arrayJSONSchemaPropertyInputItems.Type {
	case components.ArrayJSONSchemaPropertyInputItemsTypeLiteralJSONSchemaProperty:
		// arrayJSONSchemaPropertyInputItems.LiteralJSONSchemaProperty is populated
	case components.ArrayJSONSchemaPropertyInputItemsTypeObjectJSONSchemaPropertyInput:
		// arrayJSONSchemaPropertyInputItems.ObjectJSONSchemaPropertyInput is populated
	case components.ArrayJSONSchemaPropertyInputItemsTypeArrayJSONSchemaPropertyInput:
		// arrayJSONSchemaPropertyInputItems.ArrayJSONSchemaPropertyInput is populated
}
```
