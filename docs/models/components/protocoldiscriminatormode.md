# ProtocolDiscriminatorMode

How to attach protocol_discriminator. 'prefix' prepends the octet to the hex payload (User-to-User=XX<hex>;encoding=hex). 'pd_parameter' sends it as a separate parameter (User-to-User=<hex>;pd=XX;encoding=hex). Ignored when protocol_discriminator is unset.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProtocolDiscriminatorModePrefix

// Open enum: custom values can be created with a direct type cast
custom := components.ProtocolDiscriminatorMode("custom_value")
```


## Values

| Name                                   | Value                                  |
| -------------------------------------- | -------------------------------------- |
| `ProtocolDiscriminatorModePrefix`      | prefix                                 |
| `ProtocolDiscriminatorModePdParameter` | pd_parameter                           |