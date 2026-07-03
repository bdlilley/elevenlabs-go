# ConstantSchemaOverrideConstantValue1


## Supported Types

### 

```go
constantSchemaOverrideConstantValue1 := components.CreateConstantSchemaOverrideConstantValue1Str(string{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue1 := components.CreateConstantSchemaOverrideConstantValue1Integer(int64{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue1 := components.CreateConstantSchemaOverrideConstantValue1Number(float64{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue1 := components.CreateConstantSchemaOverrideConstantValue1Boolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch constantSchemaOverrideConstantValue1.Type {
	case components.ConstantSchemaOverrideConstantValue1TypeStr:
		// constantSchemaOverrideConstantValue1.Str is populated
	case components.ConstantSchemaOverrideConstantValue1TypeInteger:
		// constantSchemaOverrideConstantValue1.Integer is populated
	case components.ConstantSchemaOverrideConstantValue1TypeNumber:
		// constantSchemaOverrideConstantValue1.Number is populated
	case components.ConstantSchemaOverrideConstantValue1TypeBoolean:
		// constantSchemaOverrideConstantValue1.Boolean is populated
}
```
