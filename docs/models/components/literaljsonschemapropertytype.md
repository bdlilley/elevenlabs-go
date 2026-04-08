# LiteralJSONSchemaPropertyType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.LiteralJSONSchemaPropertyTypeBoolean

// Open enum: custom values can be created with a direct type cast
custom := components.LiteralJSONSchemaPropertyType("custom_value")
```


## Values

| Name                                   | Value                                  |
| -------------------------------------- | -------------------------------------- |
| `LiteralJSONSchemaPropertyTypeBoolean` | boolean                                |
| `LiteralJSONSchemaPropertyTypeString`  | string                                 |
| `LiteralJSONSchemaPropertyTypeInteger` | integer                                |
| `LiteralJSONSchemaPropertyTypeNumber`  | number                                 |