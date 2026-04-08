# SafetyControl

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SafetyControlNone

// Open enum: custom values can be created with a direct type cast
custom := components.SafetyControl("custom_value")
```


## Values

| Name                             | Value                            |
| -------------------------------- | -------------------------------- |
| `SafetyControlNone`              | NONE                             |
| `SafetyControlBan`               | BAN                              |
| `SafetyControlCaptcha`           | CAPTCHA                          |
| `SafetyControlEnterpriseBan`     | ENTERPRISE_BAN                   |
| `SafetyControlEnterpriseCaptcha` | ENTERPRISE_CAPTCHA               |