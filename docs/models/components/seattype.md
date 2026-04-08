# SeatType

Seat types for workspace members.
Lite Member is equivalent to Basic Seat in the web application.
Member is equivalent to Full Seat in the web application.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.SeatTypeWorkspaceAdmin

// Open enum: custom values can be created with a direct type cast
custom := components.SeatType("custom_value")
```


## Values

| Name                          | Value                         |
| ----------------------------- | ----------------------------- |
| `SeatTypeWorkspaceAdmin`      | workspace_admin               |
| `SeatTypeWorkspaceMember`     | workspace_member              |
| `SeatTypeWorkspaceLiteMember` | workspace_lite_member         |