# ConstantSchemaOverrideConstantValue

The constant value to use


## Supported Types

### 

```go
constantSchemaOverrideConstantValue := components.CreateConstantSchemaOverrideConstantValueStr(string{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue := components.CreateConstantSchemaOverrideConstantValueInteger(int64{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue := components.CreateConstantSchemaOverrideConstantValueNumber(float64{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue := components.CreateConstantSchemaOverrideConstantValueBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch constantSchemaOverrideConstantValue.Type {
	case components.ConstantSchemaOverrideConstantValueTypeStr:
		// constantSchemaOverrideConstantValue.Str is populated
	case components.ConstantSchemaOverrideConstantValueTypeInteger:
		// constantSchemaOverrideConstantValue.Integer is populated
	case components.ConstantSchemaOverrideConstantValueTypeNumber:
		// constantSchemaOverrideConstantValue.Number is populated
	case components.ConstantSchemaOverrideConstantValueTypeBoolean:
		// constantSchemaOverrideConstantValue.Boolean is populated
	default:
		// Unknown type - use constantSchemaOverrideConstantValue.GetUnknownRaw() for raw JSON
}
```
