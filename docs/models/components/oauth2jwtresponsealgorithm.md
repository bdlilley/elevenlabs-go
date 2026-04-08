# OAuth2JWTResponseAlgorithm

JWT signing algorithm

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.OAuth2JWTResponseAlgorithmHs256

// Open enum: custom values can be created with a direct type cast
custom := components.OAuth2JWTResponseAlgorithm("custom_value")
```


## Values

| Name                              | Value                             |
| --------------------------------- | --------------------------------- |
| `OAuth2JWTResponseAlgorithmHs256` | HS256                             |
| `OAuth2JWTResponseAlgorithmHs384` | HS384                             |
| `OAuth2JWTResponseAlgorithmHs512` | HS512                             |
| `OAuth2JWTResponseAlgorithmRs256` | RS256                             |
| `OAuth2JWTResponseAlgorithmRs384` | RS384                             |
| `OAuth2JWTResponseAlgorithmRs512` | RS512                             |