# ProjectResponseModelState

The state of the project.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProjectResponseModelStateCreating

// Open enum: custom values can be created with a direct type cast
custom := components.ProjectResponseModelState("custom_value")
```


## Values

| Name                                  | Value                                 |
| ------------------------------------- | ------------------------------------- |
| `ProjectResponseModelStateCreating`   | creating                              |
| `ProjectResponseModelStateDefault`    | default                               |
| `ProjectResponseModelStateConverting` | converting                            |
| `ProjectResponseModelStateInQueue`    | in_queue                              |