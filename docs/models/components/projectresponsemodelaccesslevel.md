# ProjectResponseModelAccessLevel

The access level of the project.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProjectResponseModelAccessLevelAdmin

// Open enum: custom values can be created with a direct type cast
custom := components.ProjectResponseModelAccessLevel("custom_value")
```


## Values

| Name                                       | Value                                      |
| ------------------------------------------ | ------------------------------------------ |
| `ProjectResponseModelAccessLevelAdmin`     | admin                                      |
| `ProjectResponseModelAccessLevelEditor`    | editor                                     |
| `ProjectResponseModelAccessLevelCommenter` | commenter                                  |
| `ProjectResponseModelAccessLevelViewer`    | viewer                                     |