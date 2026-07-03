# EntryBehavior

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.EntryBehaviorGenerateImmediately

// Open enum: custom values can be created with a direct type cast
custom := components.EntryBehavior("custom_value")
```


## Values

| Name                               | Value                              |
| ---------------------------------- | ---------------------------------- |
| `EntryBehaviorGenerateImmediately` | generate_immediately               |
| `EntryBehaviorWaitForUser`         | wait_for_user                      |
| `EntryBehaviorAuto`                | auto                               |