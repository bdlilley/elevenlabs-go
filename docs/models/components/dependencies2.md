# Dependencies2


## Supported Types

### DependentAvailableAgentIdentifier

```go
dependencies2 := components.CreateDependencies2Available(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
dependencies2 := components.CreateDependencies2Unknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch dependencies2.Type {
	case components.Dependencies2TypeAvailable:
		// dependencies2.DependentAvailableAgentIdentifier is populated
	case components.Dependencies2TypeUnknown:
		// dependencies2.DependentUnknownAgentIdentifier is populated
}
```
