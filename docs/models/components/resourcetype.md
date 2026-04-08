# ResourceType

The type of resource.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ResourceTypeRead

// Open enum: custom values can be created with a direct type cast
custom := components.ResourceType("custom_value")
```


## Values

| Name                     | Value                    |
| ------------------------ | ------------------------ |
| `ResourceTypeRead`       | read                     |
| `ResourceTypeCollection` | collection               |