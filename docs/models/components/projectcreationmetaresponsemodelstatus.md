# ProjectCreationMetaResponseModelStatus

The status of the project creation action.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProjectCreationMetaResponseModelStatusPending

// Open enum: custom values can be created with a direct type cast
custom := components.ProjectCreationMetaResponseModelStatus("custom_value")
```


## Values

| Name                                             | Value                                            |
| ------------------------------------------------ | ------------------------------------------------ |
| `ProjectCreationMetaResponseModelStatusPending`  | pending                                          |
| `ProjectCreationMetaResponseModelStatusCreating` | creating                                         |
| `ProjectCreationMetaResponseModelStatusFinished` | finished                                         |
| `ProjectCreationMetaResponseModelStatusFailed`   | failed                                           |