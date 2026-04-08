# ReferencedToolCommonModelType

The type of the tool

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ReferencedToolCommonModelTypeSystem

// Open enum: custom values can be created with a direct type cast
custom := components.ReferencedToolCommonModelType("custom_value")
```


## Values

| Name                                                 | Value                                                |
| ---------------------------------------------------- | ---------------------------------------------------- |
| `ReferencedToolCommonModelTypeSystem`                | system                                               |
| `ReferencedToolCommonModelTypeWebhook`               | webhook                                              |
| `ReferencedToolCommonModelTypeClient`                | client                                               |
| `ReferencedToolCommonModelTypeWorkflow`              | workflow                                             |
| `ReferencedToolCommonModelTypeAPIIntegrationWebhook` | api_integration_webhook                              |
| `ReferencedToolCommonModelTypeMcp`                   | mcp                                                  |