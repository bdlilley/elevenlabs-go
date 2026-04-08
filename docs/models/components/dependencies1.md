# Dependencies1


## Supported Types

### DependentAvailableToolIdentifier

```go
dependencies1 := components.CreateDependencies1Available(components.DependentAvailableToolIdentifier{/* values here */})
```

### DependentUnknownToolIdentifier

```go
dependencies1 := components.CreateDependencies1Unknown(components.DependentUnknownToolIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch dependencies1.Type {
	case components.Dependencies1TypeAvailable:
		// dependencies1.DependentAvailableToolIdentifier is populated
	case components.Dependencies1TypeUnknown:
		// dependencies1.DependentUnknownToolIdentifier is populated
}
```
