# ObjectJSONSchemaPropertyInputProperties


## Supported Types

### LiteralJSONSchemaProperty

```go
objectJSONSchemaPropertyInputProperties := components.CreateObjectJSONSchemaPropertyInputPropertiesLiteralJSONSchemaProperty(components.LiteralJSONSchemaProperty{/* values here */})
```

### ObjectJSONSchemaPropertyInput

```go
objectJSONSchemaPropertyInputProperties := components.CreateObjectJSONSchemaPropertyInputPropertiesObjectJSONSchemaPropertyInput(components.ObjectJSONSchemaPropertyInput{/* values here */})
```

### ArrayJSONSchemaPropertyInput

```go
objectJSONSchemaPropertyInputProperties := components.CreateObjectJSONSchemaPropertyInputPropertiesArrayJSONSchemaPropertyInput(components.ArrayJSONSchemaPropertyInput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch objectJSONSchemaPropertyInputProperties.Type {
	case components.ObjectJSONSchemaPropertyInputPropertiesTypeLiteralJSONSchemaProperty:
		// objectJSONSchemaPropertyInputProperties.LiteralJSONSchemaProperty is populated
	case components.ObjectJSONSchemaPropertyInputPropertiesTypeObjectJSONSchemaPropertyInput:
		// objectJSONSchemaPropertyInputProperties.ObjectJSONSchemaPropertyInput is populated
	case components.ObjectJSONSchemaPropertyInputPropertiesTypeArrayJSONSchemaPropertyInput:
		// objectJSONSchemaPropertyInputProperties.ArrayJSONSchemaPropertyInput is populated
}
```
