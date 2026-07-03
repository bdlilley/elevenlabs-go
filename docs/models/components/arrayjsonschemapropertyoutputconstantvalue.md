# ArrayJSONSchemaPropertyOutputConstantValue


## Supported Types

### 

```go
arrayJSONSchemaPropertyOutputConstantValue := components.CreateArrayJSONSchemaPropertyOutputConstantValueStr(string{/* values here */})
```

### 

```go
arrayJSONSchemaPropertyOutputConstantValue := components.CreateArrayJSONSchemaPropertyOutputConstantValueInteger(int64{/* values here */})
```

### 

```go
arrayJSONSchemaPropertyOutputConstantValue := components.CreateArrayJSONSchemaPropertyOutputConstantValueNumber(float64{/* values here */})
```

### 

```go
arrayJSONSchemaPropertyOutputConstantValue := components.CreateArrayJSONSchemaPropertyOutputConstantValueBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch arrayJSONSchemaPropertyOutputConstantValue.Type {
	case components.ArrayJSONSchemaPropertyOutputConstantValueTypeStr:
		// arrayJSONSchemaPropertyOutputConstantValue.Str is populated
	case components.ArrayJSONSchemaPropertyOutputConstantValueTypeInteger:
		// arrayJSONSchemaPropertyOutputConstantValue.Integer is populated
	case components.ArrayJSONSchemaPropertyOutputConstantValueTypeNumber:
		// arrayJSONSchemaPropertyOutputConstantValue.Number is populated
	case components.ArrayJSONSchemaPropertyOutputConstantValueTypeBoolean:
		// arrayJSONSchemaPropertyOutputConstantValue.Boolean is populated
}
```
