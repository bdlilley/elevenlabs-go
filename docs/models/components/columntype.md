# ColumnType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ColumnTypeString

// Open enum: custom values can be created with a direct type cast
custom := components.ColumnType("custom_value")
```


## Values

| Name                 | Value                |
| -------------------- | -------------------- |
| `ColumnTypeString`   | String               |
| `ColumnTypeFloat`    | Float                |
| `ColumnTypeDateTime` | DateTime             |
| `ColumnTypeInt`      | Int                  |
| `ColumnTypeBool`     | Bool                 |
| `ColumnTypeJSON`     | JSON                 |
| `ColumnTypeMap`      | Map                  |