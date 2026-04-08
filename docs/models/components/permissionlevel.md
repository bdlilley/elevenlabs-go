# PermissionLevel

The permission level to grant to the group

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.PermissionLevelAdmin

// Open enum: custom values can be created with a direct type cast
custom := components.PermissionLevel("custom_value")
```


## Values

| Name                    | Value                   |
| ----------------------- | ----------------------- |
| `PermissionLevelAdmin`  | admin                   |
| `PermissionLevelEditor` | editor                  |
| `PermissionLevelViewer` | viewer                  |