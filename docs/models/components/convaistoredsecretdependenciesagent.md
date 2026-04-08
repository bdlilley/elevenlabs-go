# ConvAIStoredSecretDependenciesAgent


## Supported Types

### DependentAvailableAgentIdentifier

```go
convAIStoredSecretDependenciesAgent := components.CreateConvAIStoredSecretDependenciesAgentAvailable(components.DependentAvailableAgentIdentifier{/* values here */})
```

### DependentUnknownAgentIdentifier

```go
convAIStoredSecretDependenciesAgent := components.CreateConvAIStoredSecretDependenciesAgentUnknown(components.DependentUnknownAgentIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch convAIStoredSecretDependenciesAgent.Type {
	case components.ConvAIStoredSecretDependenciesAgentTypeAvailable:
		// convAIStoredSecretDependenciesAgent.DependentAvailableAgentIdentifier is populated
	case components.ConvAIStoredSecretDependenciesAgentTypeUnknown:
		// convAIStoredSecretDependenciesAgent.DependentUnknownAgentIdentifier is populated
}
```
