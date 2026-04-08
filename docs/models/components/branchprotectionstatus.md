# BranchProtectionStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BranchProtectionStatusWriterPermsRequired

// Open enum: custom values can be created with a direct type cast
custom := components.BranchProtectionStatus("custom_value")
```


## Values

| Name                                        | Value                                       |
| ------------------------------------------- | ------------------------------------------- |
| `BranchProtectionStatusWriterPermsRequired` | writer_perms_required                       |
| `BranchProtectionStatusAdminPermsRequired`  | admin_perms_required                        |