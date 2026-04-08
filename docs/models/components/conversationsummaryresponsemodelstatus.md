# ConversationSummaryResponseModelStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ConversationSummaryResponseModelStatusInitiated

// Open enum: custom values can be created with a direct type cast
custom := components.ConversationSummaryResponseModelStatus("custom_value")
```


## Values

| Name                                               | Value                                              |
| -------------------------------------------------- | -------------------------------------------------- |
| `ConversationSummaryResponseModelStatusInitiated`  | initiated                                          |
| `ConversationSummaryResponseModelStatusInProgress` | in-progress                                        |
| `ConversationSummaryResponseModelStatusProcessing` | processing                                         |
| `ConversationSummaryResponseModelStatusDone`       | done                                               |
| `ConversationSummaryResponseModelStatusFailed`     | failed                                             |