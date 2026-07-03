# Currency

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.CurrencyUsd

// Open enum: custom values can be created with a direct type cast
custom := components.Currency("custom_value")
```


## Values

| Name          | Value         |
| ------------- | ------------- |
| `CurrencyUsd` | usd           |
| `CurrencyEur` | eur           |
| `CurrencyInr` | inr           |
| `CurrencyPln` | pln           |