# AnonymousAccessLevelOverride

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AnonymousAccessLevelOverrideAdmin

// Open enum: custom values can be created with a direct type cast
custom := components.AnonymousAccessLevelOverride("custom_value")
```


## Values

| Name                                    | Value                                   |
| --------------------------------------- | --------------------------------------- |
| `AnonymousAccessLevelOverrideAdmin`     | admin                                   |
| `AnonymousAccessLevelOverrideEditor`    | editor                                  |
| `AnonymousAccessLevelOverrideCommenter` | commenter                               |
| `AnonymousAccessLevelOverrideViewer`    | viewer                                  |