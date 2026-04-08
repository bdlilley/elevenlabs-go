# WebhookToolAPISchemaConfigOutputContentType

Content type for the request body. Only applies to POST/PUT/PATCH requests.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.WebhookToolAPISchemaConfigOutputContentTypeApplicationJSON

// Open enum: custom values can be created with a direct type cast
custom := components.WebhookToolAPISchemaConfigOutputContentType("custom_value")
```


## Values

| Name                                                                       | Value                                                                      |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `WebhookToolAPISchemaConfigOutputContentTypeApplicationJSON`               | application/json                                                           |
| `WebhookToolAPISchemaConfigOutputContentTypeApplicationXWwwFormUrlencoded` | application/x-www-form-urlencoded                                          |