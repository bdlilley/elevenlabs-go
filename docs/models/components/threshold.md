# Threshold


## Supported Types

### 

```go
threshold := components.CreateThresholdNumber(float64{/* values here */})
```

### ThresholdEnum

```go
threshold := components.CreateThresholdThresholdEnum(components.ThresholdEnum{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch threshold.Type {
	case components.ThresholdTypeNumber:
		// threshold.Number is populated
	case components.ThresholdTypeThresholdEnum:
		// threshold.ThresholdEnum is populated
	default:
		// Unknown type - use threshold.GetUnknownRaw() for raw JSON
}
```
