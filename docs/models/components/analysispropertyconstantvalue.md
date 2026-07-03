# AnalysisPropertyConstantValue

A constant value to use for this property. Mutually exclusive with description, dynamic_variable, is_system_provided, and is_omitted.


## Supported Types

### 

```go
analysisPropertyConstantValue := components.CreateAnalysisPropertyConstantValueStr(string{/* values here */})
```

### 

```go
analysisPropertyConstantValue := components.CreateAnalysisPropertyConstantValueInteger(int64{/* values here */})
```

### 

```go
analysisPropertyConstantValue := components.CreateAnalysisPropertyConstantValueNumber(float64{/* values here */})
```

### 

```go
analysisPropertyConstantValue := components.CreateAnalysisPropertyConstantValueBoolean(bool{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch analysisPropertyConstantValue.Type {
	case components.AnalysisPropertyConstantValueTypeStr:
		// analysisPropertyConstantValue.Str is populated
	case components.AnalysisPropertyConstantValueTypeInteger:
		// analysisPropertyConstantValue.Integer is populated
	case components.AnalysisPropertyConstantValueTypeNumber:
		// analysisPropertyConstantValue.Number is populated
	case components.AnalysisPropertyConstantValueTypeBoolean:
		// analysisPropertyConstantValue.Boolean is populated
}
```
