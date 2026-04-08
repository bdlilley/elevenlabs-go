# MCPServerConfigOutputAuthConnection

Optional auth connection to use for authentication with this MCP server


## Supported Types

### AuthConnectionLocator

```go
mcpServerConfigOutputAuthConnection := components.CreateMCPServerConfigOutputAuthConnectionAuthConnectionLocator(components.AuthConnectionLocator{/* values here */})
```

### EnvironmentAuthConnectionLocator

```go
mcpServerConfigOutputAuthConnection := components.CreateMCPServerConfigOutputAuthConnectionEnvironmentAuthConnectionLocator(components.EnvironmentAuthConnectionLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigOutputAuthConnection.Type {
	case components.MCPServerConfigOutputAuthConnectionTypeAuthConnectionLocator:
		// mcpServerConfigOutputAuthConnection.AuthConnectionLocator is populated
	case components.MCPServerConfigOutputAuthConnectionTypeEnvironmentAuthConnectionLocator:
		// mcpServerConfigOutputAuthConnection.EnvironmentAuthConnectionLocator is populated
	default:
		// Unknown type - use mcpServerConfigOutputAuthConnection.GetUnknownRaw() for raw JSON
}
```
