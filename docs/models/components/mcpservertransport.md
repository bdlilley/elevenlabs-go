# MCPServerTransport

Supported MCP server transport types.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.MCPServerTransportSse

// Open enum: custom values can be created with a direct type cast
custom := components.MCPServerTransport("custom_value")
```


## Values

| Name                               | Value                              |
| ---------------------------------- | ---------------------------------- |
| `MCPServerTransportSse`            | SSE                                |
| `MCPServerTransportStreamableHTTP` | STREAMABLE_HTTP                    |