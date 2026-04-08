# OAuthConnectionStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.OAuthConnectionStatusActive

// Open enum: custom values can be created with a direct type cast
custom := components.OAuthConnectionStatus("custom_value")
```


## Values

| Name                                 | Value                                |
| ------------------------------------ | ------------------------------------ |
| `OAuthConnectionStatusActive`        | active                               |
| `OAuthConnectionStatusRefreshFailed` | refresh_failed                       |
| `OAuthConnectionStatusRevoked`       | revoked                              |