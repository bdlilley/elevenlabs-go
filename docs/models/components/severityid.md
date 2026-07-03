# SeverityID

OCSF Severity levels.

Spec: https://schema.ocsf.io/1.6.0/objects/severity_id

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SeverityIDZero

// Open enum: custom values can be created with a direct type cast
custom := components.SeverityID(999)
```


## Values

| Name                   | Value                  |
| ---------------------- | ---------------------- |
| `SeverityIDZero`       | 0                      |
| `SeverityIDOne`        | 1                      |
| `SeverityIDTwo`        | 2                      |
| `SeverityIDThree`      | 3                      |
| `SeverityIDFour`       | 4                      |
| `SeverityIDFive`       | 5                      |
| `SeverityIDSix`        | 6                      |
| `SeverityIDNinetyNine` | 99                     |