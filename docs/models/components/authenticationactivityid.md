# AuthenticationActivityID

OCSF Activity IDs for Authentication [3002] events.

Spec: https://schema.ocsf.io/1.6.0/classes/authentication

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AuthenticationActivityIDZero

// Open enum: custom values can be created with a direct type cast
custom := components.AuthenticationActivityID(999)
```


## Values

| Name                                 | Value                                |
| ------------------------------------ | ------------------------------------ |
| `AuthenticationActivityIDZero`       | 0                                    |
| `AuthenticationActivityIDOne`        | 1                                    |
| `AuthenticationActivityIDTwo`        | 2                                    |
| `AuthenticationActivityIDThree`      | 3                                    |
| `AuthenticationActivityIDFour`       | 4                                    |
| `AuthenticationActivityIDFive`       | 5                                    |
| `AuthenticationActivityIDSix`        | 6                                    |
| `AuthenticationActivityIDSeven`      | 7                                    |
| `AuthenticationActivityIDNinetyNine` | 99                                   |