# TurnEagerness

Agent's eagerness to respond. Higher values make agent wait for higher turn probability.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.TurnEagernessPatient

// Open enum: custom values can be created with a direct type cast
custom := components.TurnEagerness("custom_value")
```


## Values

| Name                   | Value                  |
| ---------------------- | ---------------------- |
| `TurnEagernessPatient` | patient                |
| `TurnEagernessNormal`  | normal                 |
| `TurnEagernessEager`   | eager                  |