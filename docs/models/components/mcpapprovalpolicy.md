# MCPApprovalPolicy

Defines the MCP server-level approval policy for tool execution.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.MCPApprovalPolicyAutoApproveAll

// Open enum: custom values can be created with a direct type cast
custom := components.MCPApprovalPolicy("custom_value")
```


## Values

| Name                                      | Value                                     |
| ----------------------------------------- | ----------------------------------------- |
| `MCPApprovalPolicyAutoApproveAll`         | auto_approve_all                          |
| `MCPApprovalPolicyRequireApprovalAll`     | require_approval_all                      |
| `MCPApprovalPolicyRequireApprovalPerTool` | require_approval_per_tool                 |