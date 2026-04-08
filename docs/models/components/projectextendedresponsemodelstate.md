# ProjectExtendedResponseModelState

The state of the project.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProjectExtendedResponseModelStateCreating

// Open enum: custom values can be created with a direct type cast
custom := components.ProjectExtendedResponseModelState("custom_value")
```


## Values

| Name                                          | Value                                         |
| --------------------------------------------- | --------------------------------------------- |
| `ProjectExtendedResponseModelStateCreating`   | creating                                      |
| `ProjectExtendedResponseModelStateDefault`    | default                                       |
| `ProjectExtendedResponseModelStateConverting` | converting                                    |
| `ProjectExtendedResponseModelStateInQueue`    | in_queue                                      |