# AuthConnectionDependenciesTool


## Supported Types

### DependentAvailableToolIdentifier

```go
authConnectionDependenciesTool := components.CreateAuthConnectionDependenciesToolAvailable(components.DependentAvailableToolIdentifier{/* values here */})
```

### DependentUnknownToolIdentifier

```go
authConnectionDependenciesTool := components.CreateAuthConnectionDependenciesToolUnknown(components.DependentUnknownToolIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch authConnectionDependenciesTool.Type {
	case components.AuthConnectionDependenciesToolTypeAvailable:
		// authConnectionDependenciesTool.DependentAvailableToolIdentifier is populated
	case components.AuthConnectionDependenciesToolTypeUnknown:
		// authConnectionDependenciesTool.DependentUnknownToolIdentifier is populated
	default:
		// Unknown type - use authConnectionDependenciesTool.GetUnknownRaw() for raw JSON
}
```
