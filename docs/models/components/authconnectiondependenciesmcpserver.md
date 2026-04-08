# AuthConnectionDependenciesMcpServer


## Supported Types

### DependentAvailableMCPServerIdentifier

```go
authConnectionDependenciesMcpServer := components.CreateAuthConnectionDependenciesMcpServerAvailable(components.DependentAvailableMCPServerIdentifier{/* values here */})
```

### DependentUnknownMCPServerIdentifier

```go
authConnectionDependenciesMcpServer := components.CreateAuthConnectionDependenciesMcpServerUnknown(components.DependentUnknownMCPServerIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch authConnectionDependenciesMcpServer.Type {
	case components.AuthConnectionDependenciesMcpServerTypeAvailable:
		// authConnectionDependenciesMcpServer.DependentAvailableMCPServerIdentifier is populated
	case components.AuthConnectionDependenciesMcpServerTypeUnknown:
		// authConnectionDependenciesMcpServer.DependentUnknownMCPServerIdentifier is populated
}
```
