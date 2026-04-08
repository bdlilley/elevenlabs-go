# ResourceAccessInfoRole

The role of the user making the request

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ResourceAccessInfoRoleAdmin

// Open enum: custom values can be created with a direct type cast
custom := components.ResourceAccessInfoRole("custom_value")
```


## Values

| Name                              | Value                             |
| --------------------------------- | --------------------------------- |
| `ResourceAccessInfoRoleAdmin`     | admin                             |
| `ResourceAccessInfoRoleEditor`    | editor                            |
| `ResourceAccessInfoRoleCommenter` | commenter                         |
| `ResourceAccessInfoRoleViewer`    | viewer                            |