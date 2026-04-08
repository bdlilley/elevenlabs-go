# WebhookToolAPISchemaConfigOutputMethod

The HTTP method to use for the webhook

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.WebhookToolAPISchemaConfigOutputMethodGet

// Open enum: custom values can be created with a direct type cast
custom := components.WebhookToolAPISchemaConfigOutputMethod("custom_value")
```


## Values

| Name                                           | Value                                          |
| ---------------------------------------------- | ---------------------------------------------- |
| `WebhookToolAPISchemaConfigOutputMethodGet`    | GET                                            |
| `WebhookToolAPISchemaConfigOutputMethodPost`   | POST                                           |
| `WebhookToolAPISchemaConfigOutputMethodPut`    | PUT                                            |
| `WebhookToolAPISchemaConfigOutputMethodPatch`  | PATCH                                          |
| `WebhookToolAPISchemaConfigOutputMethodDelete` | DELETE                                         |