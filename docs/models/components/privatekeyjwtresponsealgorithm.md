# PrivateKeyJWTResponseAlgorithm

JWT signing algorithm

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.PrivateKeyJWTResponseAlgorithmHs256

// Open enum: custom values can be created with a direct type cast
custom := components.PrivateKeyJWTResponseAlgorithm("custom_value")
```


## Values

| Name                                  | Value                                 |
| ------------------------------------- | ------------------------------------- |
| `PrivateKeyJWTResponseAlgorithmHs256` | HS256                                 |
| `PrivateKeyJWTResponseAlgorithmHs384` | HS384                                 |
| `PrivateKeyJWTResponseAlgorithmHs512` | HS512                                 |
| `PrivateKeyJWTResponseAlgorithmRs256` | RS256                                 |
| `PrivateKeyJWTResponseAlgorithmRs384` | RS384                                 |
| `PrivateKeyJWTResponseAlgorithmRs512` | RS512                                 |