# VoiceSharingResponseModelReviewStatus

The review status of the voice.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.VoiceSharingResponseModelReviewStatusNotRequested

// Open enum: custom values can be created with a direct type cast
custom := components.VoiceSharingResponseModelReviewStatus("custom_value")
```


## Values

| Name                                                      | Value                                                     |
| --------------------------------------------------------- | --------------------------------------------------------- |
| `VoiceSharingResponseModelReviewStatusNotRequested`       | not_requested                                             |
| `VoiceSharingResponseModelReviewStatusPending`            | pending                                                   |
| `VoiceSharingResponseModelReviewStatusDeclined`           | declined                                                  |
| `VoiceSharingResponseModelReviewStatusAllowed`            | allowed                                                   |
| `VoiceSharingResponseModelReviewStatusAllowedWithChanges` | allowed_with_changes                                      |