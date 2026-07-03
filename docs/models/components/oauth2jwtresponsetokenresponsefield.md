# OAuth2JWTResponseTokenResponseField

Token field to extract from the token endpoint response.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.OAuth2JWTResponseTokenResponseFieldAccessToken

// Open enum: custom values can be created with a direct type cast
custom := components.OAuth2JWTResponseTokenResponseField("custom_value")
```


## Values

| Name                                             | Value                                            |
| ------------------------------------------------ | ------------------------------------------------ |
| `OAuth2JWTResponseTokenResponseFieldAccessToken` | access_token                                     |
| `OAuth2JWTResponseTokenResponseFieldIDToken`     | id_token                                         |