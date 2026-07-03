# StatusID

OCSF Status levels.

Spec: https://schema.ocsf.io/1.6.0/objects/status_id

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.StatusIDZero

// Open enum: custom values can be created with a direct type cast
custom := components.StatusID(999)
```


## Values

| Name                 | Value                |
| -------------------- | -------------------- |
| `StatusIDZero`       | 0                    |
| `StatusIDOne`        | 1                    |
| `StatusIDTwo`        | 2                    |
| `StatusIDNinetyNine` | 99                   |