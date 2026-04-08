# EnterEffect

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.EnterEffectNone

// Open enum: custom values can be created with a direct type cast
custom := components.EnterEffect("custom_value")
```


## Values

| Name                     | Value                    |
| ------------------------ | ------------------------ |
| `EnterEffectNone`        | none                     |
| `EnterEffectFade`        | fade                     |
| `EnterEffectFloat`       | float                    |
| `EnterEffectGentleFloat` | gentle_float             |
| `EnterEffectZoomIn`      | zoom_in                  |
| `EnterEffectDrop`        | drop                     |
| `EnterEffectSlideLeft`   | slide_left               |
| `EnterEffectSlideRight`  | slide_right              |
| `EnterEffectSlideUp`     | slide_up                 |
| `EnterEffectSlideDown`   | slide_down               |
| `EnterEffectPop`         | pop                      |
| `EnterEffectBounce`      | bounce                   |
| `EnterEffectSpin`        | spin                     |
| `EnterEffectSlideBounce` | slide_bounce             |