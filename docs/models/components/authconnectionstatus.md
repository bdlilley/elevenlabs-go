# AuthConnectionStatus

Single status field shared by every auth type's stored credential.

OAuth values (``REFRESH_FAILED``, ``REVOKED``) are written by the OAuth
token-manager refresh path. ``CREDENTIAL_INVALID`` is written by the
tool execution path when an upstream response matches a credential's
``failure_signatures`` entry (Bearer, Basic auth, etc.).

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AuthConnectionStatusActive

// Open enum: custom values can be created with a direct type cast
custom := components.AuthConnectionStatus("custom_value")
```


## Values

| Name                                    | Value                                   |
| --------------------------------------- | --------------------------------------- |
| `AuthConnectionStatusActive`            | active                                  |
| `AuthConnectionStatusRefreshFailed`     | refresh_failed                          |
| `AuthConnectionStatusRevoked`           | revoked                                 |
| `AuthConnectionStatusCredentialInvalid` | credential_invalid                      |