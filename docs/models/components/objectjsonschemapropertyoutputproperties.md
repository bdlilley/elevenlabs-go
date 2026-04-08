# ObjectJSONSchemaPropertyOutputProperties


## Supported Types

### LiteralJSONSchemaProperty

```go
objectJSONSchemaPropertyOutputProperties := components.CreateObjectJSONSchemaPropertyOutputPropertiesLiteralJSONSchemaProperty(components.LiteralJSONSchemaProperty{/* values here */})
```

### ObjectJSONSchemaPropertyOutput

```go
objectJSONSchemaPropertyOutputProperties := components.CreateObjectJSONSchemaPropertyOutputPropertiesObjectJSONSchemaPropertyOutput(components.ObjectJSONSchemaPropertyOutput{/* values here */})
```

### ArrayJSONSchemaPropertyOutput

```go
objectJSONSchemaPropertyOutputProperties := components.CreateObjectJSONSchemaPropertyOutputPropertiesArrayJSONSchemaPropertyOutput(components.ArrayJSONSchemaPropertyOutput{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch objectJSONSchemaPropertyOutputProperties.Type {
	case components.ObjectJSONSchemaPropertyOutputPropertiesTypeLiteralJSONSchemaProperty:
		// objectJSONSchemaPropertyOutputProperties.LiteralJSONSchemaProperty is populated
	case components.ObjectJSONSchemaPropertyOutputPropertiesTypeObjectJSONSchemaPropertyOutput:
		// objectJSONSchemaPropertyOutputProperties.ObjectJSONSchemaPropertyOutput is populated
	case components.ObjectJSONSchemaPropertyOutputPropertiesTypeArrayJSONSchemaPropertyOutput:
		// objectJSONSchemaPropertyOutputProperties.ArrayJSONSchemaPropertyOutput is populated
}
```
