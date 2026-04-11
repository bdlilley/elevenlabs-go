# GroupPvcLimit


## Supported Types

### 

```go
groupPvcLimit := components.CreateGroupPvcLimitInteger(int64{/* values here */})
```

### 

```go
groupPvcLimit := components.CreateGroupPvcLimitStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch groupPvcLimit.Type {
	case components.GroupPvcLimitTypeInteger:
		// groupPvcLimit.Integer is populated
	case components.GroupPvcLimitTypeStr:
		// groupPvcLimit.Str is populated
}
```
