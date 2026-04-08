# MCPServerConfigInputAuthConnection

Optional auth connection to use for authentication with this MCP server


## Supported Types

### AuthConnectionLocator

```go
mcpServerConfigInputAuthConnection := components.CreateMCPServerConfigInputAuthConnectionAuthConnectionLocator(components.AuthConnectionLocator{/* values here */})
```

### EnvironmentAuthConnectionLocator

```go
mcpServerConfigInputAuthConnection := components.CreateMCPServerConfigInputAuthConnectionEnvironmentAuthConnectionLocator(components.EnvironmentAuthConnectionLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigInputAuthConnection.Type {
	case components.MCPServerConfigInputAuthConnectionTypeAuthConnectionLocator:
		// mcpServerConfigInputAuthConnection.AuthConnectionLocator is populated
	case components.MCPServerConfigInputAuthConnectionTypeEnvironmentAuthConnectionLocator:
		// mcpServerConfigInputAuthConnection.EnvironmentAuthConnectionLocator is populated
}
```
