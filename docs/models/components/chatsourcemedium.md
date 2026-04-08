# ChatSourceMedium

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ChatSourceMediumAudio

// Open enum: custom values can be created with a direct type cast
custom := components.ChatSourceMedium("custom_value")
```


## Values

| Name                    | Value                   |
| ----------------------- | ----------------------- |
| `ChatSourceMediumAudio` | audio                   |
| `ChatSourceMediumDtmf`  | dtmf                    |
| `ChatSourceMediumText`  | text                    |
| `ChatSourceMediumImage` | image                   |
| `ChatSourceMediumFile`  | file                    |