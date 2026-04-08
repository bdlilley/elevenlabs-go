# ToolType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ToolTypeSystem

// Open enum: custom values can be created with a direct type cast
custom := components.ToolType("custom_value")
```


## Values

| Name                            | Value                           |
| ------------------------------- | ------------------------------- |
| `ToolTypeSystem`                | system                          |
| `ToolTypeWebhook`               | webhook                         |
| `ToolTypeClient`                | client                          |
| `ToolTypeMcp`                   | mcp                             |
| `ToolTypeWorkflow`              | workflow                        |
| `ToolTypeAPIIntegrationWebhook` | api_integration_webhook         |
| `ToolTypeAPIIntegrationMcp`     | api_integration_mcp             |
| `ToolTypeSmb`                   | smb                             |