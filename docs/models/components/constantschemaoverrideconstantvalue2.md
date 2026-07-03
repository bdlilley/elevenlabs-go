# ConstantSchemaOverrideConstantValue2

The constant value to use


## Supported Types

### 

```go
constantSchemaOverrideConstantValue2 := components.CreateConstantSchemaOverrideConstantValue2Str(string{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue2 := components.CreateConstantSchemaOverrideConstantValue2Integer(int64{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue2 := components.CreateConstantSchemaOverrideConstantValue2Number(float64{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue2 := components.CreateConstantSchemaOverrideConstantValue2Boolean(bool{/* values here */})
```

### 

```go
constantSchemaOverrideConstantValue2 := components.CreateConstantSchemaOverrideConstantValue2ArrayOfConstantSchemaOverrideConstantValue1([]components.ConstantSchemaOverrideConstantValue1{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch constantSchemaOverrideConstantValue2.Type {
	case components.ConstantSchemaOverrideConstantValue2TypeStr:
		// constantSchemaOverrideConstantValue2.Str is populated
	case components.ConstantSchemaOverrideConstantValue2TypeInteger:
		// constantSchemaOverrideConstantValue2.Integer is populated
	case components.ConstantSchemaOverrideConstantValue2TypeNumber:
		// constantSchemaOverrideConstantValue2.Number is populated
	case components.ConstantSchemaOverrideConstantValue2TypeBoolean:
		// constantSchemaOverrideConstantValue2.Boolean is populated
	case components.ConstantSchemaOverrideConstantValue2TypeArrayOfConstantSchemaOverrideConstantValue1:
		// constantSchemaOverrideConstantValue2.ArrayOfConstantSchemaOverrideConstantValue1 is populated
}
```
