# MCPServerConfigUpdateRequestModelAuthConnection

Optional auth connection to use for authentication with this MCP server


## Supported Types

### AuthConnectionLocator

```go
mcpServerConfigUpdateRequestModelAuthConnection := components.CreateMCPServerConfigUpdateRequestModelAuthConnectionAuthConnectionLocator(components.AuthConnectionLocator{/* values here */})
```

### EnvironmentAuthConnectionLocator

```go
mcpServerConfigUpdateRequestModelAuthConnection := components.CreateMCPServerConfigUpdateRequestModelAuthConnectionEnvironmentAuthConnectionLocator(components.EnvironmentAuthConnectionLocator{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch mcpServerConfigUpdateRequestModelAuthConnection.Type {
	case components.MCPServerConfigUpdateRequestModelAuthConnectionTypeAuthConnectionLocator:
		// mcpServerConfigUpdateRequestModelAuthConnection.AuthConnectionLocator is populated
	case components.MCPServerConfigUpdateRequestModelAuthConnectionTypeEnvironmentAuthConnectionLocator:
		// mcpServerConfigUpdateRequestModelAuthConnection.EnvironmentAuthConnectionLocator is populated
}
```
