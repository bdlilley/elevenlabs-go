# Row


## Supported Types

### 

```go
row := components.CreateRowStr(string{/* values here */})
```

### 

```go
row := components.CreateRowInteger(int64{/* values here */})
```

### 

```go
row := components.CreateRowNumber(float64{/* values here */})
```

### 

```go
row := components.CreateRowBoolean(bool{/* values here */})
```

### 

```go
row := components.CreateRowDateTime(time.Time{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch row.Type {
	case components.RowTypeStr:
		// row.Str is populated
	case components.RowTypeInteger:
		// row.Integer is populated
	case components.RowTypeNumber:
		// row.Number is populated
	case components.RowTypeBoolean:
		// row.Boolean is populated
	case components.RowTypeDateTime:
		// row.DateTime is populated
}
```
