# IsEnabled

Whether to enable or disable the API key.


## Supported Types

### 

```go
isEnabled := components.CreateIsEnabledBoolean(bool{/* values here */})
```

### 

```go
isEnabled := components.CreateIsEnabledStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch isEnabled.Type {
	case components.IsEnabledTypeBoolean:
		// isEnabled.Boolean is populated
	case components.IsEnabledTypeStr:
		// isEnabled.Str is populated
}
```
