# VoiceSharingResponseModelStatus

The status of the voice sharing.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.VoiceSharingResponseModelStatusEnabled

// Open enum: custom values can be created with a direct type cast
custom := components.VoiceSharingResponseModelStatus("custom_value")
```


## Values

| Name                                            | Value                                           |
| ----------------------------------------------- | ----------------------------------------------- |
| `VoiceSharingResponseModelStatusEnabled`        | enabled                                         |
| `VoiceSharingResponseModelStatusDisabled`       | disabled                                        |
| `VoiceSharingResponseModelStatusCopied`         | copied                                          |
| `VoiceSharingResponseModelStatusCopiedDisabled` | copied_disabled                                 |