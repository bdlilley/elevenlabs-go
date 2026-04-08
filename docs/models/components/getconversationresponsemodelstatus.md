# GetConversationResponseModelStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.GetConversationResponseModelStatusInitiated

// Open enum: custom values can be created with a direct type cast
custom := components.GetConversationResponseModelStatus("custom_value")
```


## Values

| Name                                           | Value                                          |
| ---------------------------------------------- | ---------------------------------------------- |
| `GetConversationResponseModelStatusInitiated`  | initiated                                      |
| `GetConversationResponseModelStatusInProgress` | in-progress                                    |
| `GetConversationResponseModelStatusProcessing` | processing                                     |
| `GetConversationResponseModelStatusDone`       | done                                           |
| `GetConversationResponseModelStatusFailed`     | failed                                         |