# AccessSource

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AccessSourceCreator

// Open enum: custom values can be created with a direct type cast
custom := components.AccessSource("custom_value")
```


## Values

| Name                           | Value                          |
| ------------------------------ | ------------------------------ |
| `AccessSourceCreator`          | creator                        |
| `AccessSourceExplicit`         | explicit                       |
| `AccessSourceWorkspaceAdmin`   | workspace_admin                |
| `AccessSourceWorkspaceDefault` | workspace_default              |