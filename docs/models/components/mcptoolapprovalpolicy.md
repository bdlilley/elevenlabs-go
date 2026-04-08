# MCPToolApprovalPolicy

Defines the tool-level approval policy.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.MCPToolApprovalPolicyAutoApproved

// Open enum: custom values can be created with a direct type cast
custom := components.MCPToolApprovalPolicy("custom_value")
```


## Values

| Name                                    | Value                                   |
| --------------------------------------- | --------------------------------------- |
| `MCPToolApprovalPolicyAutoApproved`     | auto_approved                           |
| `MCPToolApprovalPolicyRequiresApproval` | requires_approval                       |