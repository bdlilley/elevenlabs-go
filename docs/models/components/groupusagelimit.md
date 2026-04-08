# GroupUsageLimit


## Supported Types

### 

```go
groupUsageLimit := components.CreateGroupUsageLimitInteger(int64{/* values here */})
```

### 

```go
groupUsageLimit := components.CreateGroupUsageLimitStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch groupUsageLimit.Type {
	case components.GroupUsageLimitTypeInteger:
		// groupUsageLimit.Integer is populated
	case components.GroupUsageLimitTypeStr:
		// groupUsageLimit.Str is populated
}
```
