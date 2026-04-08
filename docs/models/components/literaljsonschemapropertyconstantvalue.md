# LiteralJSONSchemaPropertyConstantValue

A constant value to use for this property. Mutually exclusive with description, dynamic_variable, and is_system_provided.


## Supported Types

### 

```go
literalJSONSchemaPropertyConstantValue := components.CreateLiteralJSONSchemaPropertyConstantValueStr(string{/* values here */})
```

### 

```go
literalJSONSchemaPropertyConstantValue := components.CreateLiteralJSONSchemaPropertyConstantValueInteger(int64{/* values here */})
```

### 

```go
literalJSONSchemaPropertyConstantValue := components.CreateLiteralJSONSchemaPropertyConstantValueNumber(float64{/* values here */})
```

### 

```go
literalJSONSchemaPropertyConstantValue := components.CreateLiteralJSONSchemaPropertyConstantValueBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch literalJSONSchemaPropertyConstantValue.Type {
	case components.LiteralJSONSchemaPropertyConstantValueTypeStr:
		// literalJSONSchemaPropertyConstantValue.Str is populated
	case components.LiteralJSONSchemaPropertyConstantValueTypeInteger:
		// literalJSONSchemaPropertyConstantValue.Integer is populated
	case components.LiteralJSONSchemaPropertyConstantValueTypeNumber:
		// literalJSONSchemaPropertyConstantValue.Number is populated
	case components.LiteralJSONSchemaPropertyConstantValueTypeBoolean:
		// literalJSONSchemaPropertyConstantValue.Boolean is populated
}
```
