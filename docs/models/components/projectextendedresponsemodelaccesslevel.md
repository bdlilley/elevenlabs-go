# ProjectExtendedResponseModelAccessLevel

The access level of the project.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProjectExtendedResponseModelAccessLevelAdmin

// Open enum: custom values can be created with a direct type cast
custom := components.ProjectExtendedResponseModelAccessLevel("custom_value")
```


## Values

| Name                                               | Value                                              |
| -------------------------------------------------- | -------------------------------------------------- |
| `ProjectExtendedResponseModelAccessLevelAdmin`     | admin                                              |
| `ProjectExtendedResponseModelAccessLevelEditor`    | editor                                             |
| `ProjectExtendedResponseModelAccessLevelCommenter` | commenter                                          |
| `ProjectExtendedResponseModelAccessLevelViewer`    | viewer                                             |