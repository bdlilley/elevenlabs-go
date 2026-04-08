# ConvAIStoredSecretDependenciesMcpServer


## Supported Types

### DependentAvailableMCPServerIdentifier

```go
convAIStoredSecretDependenciesMcpServer := components.CreateConvAIStoredSecretDependenciesMcpServerAvailable(components.DependentAvailableMCPServerIdentifier{/* values here */})
```

### DependentUnknownMCPServerIdentifier

```go
convAIStoredSecretDependenciesMcpServer := components.CreateConvAIStoredSecretDependenciesMcpServerUnknown(components.DependentUnknownMCPServerIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch convAIStoredSecretDependenciesMcpServer.Type {
	case components.ConvAIStoredSecretDependenciesMcpServerTypeAvailable:
		// convAIStoredSecretDependenciesMcpServer.DependentAvailableMCPServerIdentifier is populated
	case components.ConvAIStoredSecretDependenciesMcpServerTypeUnknown:
		// convAIStoredSecretDependenciesMcpServer.DependentUnknownMCPServerIdentifier is populated
	default:
		// Unknown type - use convAIStoredSecretDependenciesMcpServer.GetUnknownRaw() for raw JSON
}
```
