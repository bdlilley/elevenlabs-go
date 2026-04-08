# ShareOptionResponseModelType

The type of the principal: user, group, or service account (under 'key').

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ShareOptionResponseModelTypeUser

// Open enum: custom values can be created with a direct type cast
custom := components.ShareOptionResponseModelType("custom_value")
```


## Values

| Name                                | Value                               |
| ----------------------------------- | ----------------------------------- |
| `ShareOptionResponseModelTypeUser`  | user                                |
| `ShareOptionResponseModelTypeGroup` | group                               |
| `ShareOptionResponseModelTypeKey`   | key                                 |