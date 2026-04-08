# ConvAIStoredSecretDependenciesTool


## Supported Types

### DependentAvailableToolIdentifier

```go
convAIStoredSecretDependenciesTool := components.CreateConvAIStoredSecretDependenciesToolAvailable(components.DependentAvailableToolIdentifier{/* values here */})
```

### DependentUnknownToolIdentifier

```go
convAIStoredSecretDependenciesTool := components.CreateConvAIStoredSecretDependenciesToolUnknown(components.DependentUnknownToolIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch convAIStoredSecretDependenciesTool.Type {
	case components.ConvAIStoredSecretDependenciesToolTypeAvailable:
		// convAIStoredSecretDependenciesTool.DependentAvailableToolIdentifier is populated
	case components.ConvAIStoredSecretDependenciesToolTypeUnknown:
		// convAIStoredSecretDependenciesTool.DependentUnknownToolIdentifier is populated
}
```
