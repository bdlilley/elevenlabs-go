# ArrayJSONSchemaPropertyInputConstantValue


## Supported Types

### 

```go
arrayJSONSchemaPropertyInputConstantValue := components.CreateArrayJSONSchemaPropertyInputConstantValueStr(string{/* values here */})
```

### 

```go
arrayJSONSchemaPropertyInputConstantValue := components.CreateArrayJSONSchemaPropertyInputConstantValueInteger(int64{/* values here */})
```

### 

```go
arrayJSONSchemaPropertyInputConstantValue := components.CreateArrayJSONSchemaPropertyInputConstantValueNumber(float64{/* values here */})
```

### 

```go
arrayJSONSchemaPropertyInputConstantValue := components.CreateArrayJSONSchemaPropertyInputConstantValueBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch arrayJSONSchemaPropertyInputConstantValue.Type {
	case components.ArrayJSONSchemaPropertyInputConstantValueTypeStr:
		// arrayJSONSchemaPropertyInputConstantValue.Str is populated
	case components.ArrayJSONSchemaPropertyInputConstantValueTypeInteger:
		// arrayJSONSchemaPropertyInputConstantValue.Integer is populated
	case components.ArrayJSONSchemaPropertyInputConstantValueTypeNumber:
		// arrayJSONSchemaPropertyInputConstantValue.Number is populated
	case components.ArrayJSONSchemaPropertyInputConstantValueTypeBoolean:
		// arrayJSONSchemaPropertyInputConstantValue.Boolean is populated
}
```
