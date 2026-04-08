# AuthorizationMethod

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AuthorizationMethodInvalid

// Open enum: custom values can be created with a direct type cast
custom := components.AuthorizationMethod("custom_value")
```


## Values

| Name                                     | Value                                    |
| ---------------------------------------- | ---------------------------------------- |
| `AuthorizationMethodInvalid`             | invalid                                  |
| `AuthorizationMethodPublic`              | public                                   |
| `AuthorizationMethodAuthorizationHeader` | authorization_header                     |
| `AuthorizationMethodSignedURL`           | signed_url                               |
| `AuthorizationMethodShareableLink`       | shareable_link                           |
| `AuthorizationMethodLivekitToken`        | livekit_token                            |
| `AuthorizationMethodLivekitTokenWebsite` | livekit_token_website                    |
| `AuthorizationMethodGenesysAPIKey`       | genesys_api_key                          |
| `AuthorizationMethodWhatsapp`            | whatsapp                                 |