# ModeEnum

The mode in which to run this Dubbing job. Defaults to automatic, use manual if specifically providing a CSV transcript to use. Note that manual mode is experimental and production use is strongly discouraged.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ModeEnumAutomatic
```


## Values

| Name                | Value               |
| ------------------- | ------------------- |
| `ModeEnumAutomatic` | automatic           |
| `ModeEnumManual`    | manual              |