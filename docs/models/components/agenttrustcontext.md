# AgentTrustContext

The trust context in which the agent operates.

UNKNOWN: not yet classified (existing agents created before this feature).
LOW: serves untrusted external participants (e.g. customer support, sales) —
     outputs should be vetted and tool access scoped.
HIGH: serves the owner (e.g. personal assistant) — full tool access is appropriate.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.AgentTrustContextUnknown

// Open enum: custom values can be created with a direct type cast
custom := components.AgentTrustContext("custom_value")
```


## Values

| Name                       | Value                      |
| -------------------------- | -------------------------- |
| `AgentTrustContextUnknown` | unknown                    |
| `AgentTrustContextLow`     | low                        |
| `AgentTrustContextHigh`    | high                       |