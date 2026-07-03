# BucketingStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BucketingStatusPending

// Open enum: custom values can be created with a direct type cast
custom := components.BucketingStatus("custom_value")
```


## Values

| Name                       | Value                      |
| -------------------------- | -------------------------- |
| `BucketingStatusPending`   | pending                    |
| `BucketingStatusCompleted` | completed                  |
| `BucketingStatusFailed`    | failed                     |