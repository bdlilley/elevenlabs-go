# UserTypeID

OCSF User type IDs.

Spec: https://schema.ocsf.io/1.6.0/objects/user

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.UserTypeIDZero

// Open enum: custom values can be created with a direct type cast
custom := components.UserTypeID(999)
```


## Values

| Name                   | Value                  |
| ---------------------- | ---------------------- |
| `UserTypeIDZero`       | 0                      |
| `UserTypeIDOne`        | 1                      |
| `UserTypeIDTwo`        | 2                      |
| `UserTypeIDThree`      | 3                      |
| `UserTypeIDFour`       | 4                      |
| `UserTypeIDNinetyNine` | 99                     |