# WebhookAuthMethodType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.WebhookAuthMethodTypeHmac

// Open enum: custom values can be created with a direct type cast
custom := components.WebhookAuthMethodType("custom_value")
```


## Values

| Name                          | Value                         |
| ----------------------------- | ----------------------------- |
| `WebhookAuthMethodTypeHmac`   | hmac                          |
| `WebhookAuthMethodTypeOauth2` | oauth2                        |
| `WebhookAuthMethodTypeMtls`   | mtls                          |