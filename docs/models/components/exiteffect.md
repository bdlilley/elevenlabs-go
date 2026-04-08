# ExitEffect

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ExitEffectNone

// Open enum: custom values can be created with a direct type cast
custom := components.ExitEffect("custom_value")
```


## Values

| Name                    | Value                   |
| ----------------------- | ----------------------- |
| `ExitEffectNone`        | none                    |
| `ExitEffectFade`        | fade                    |
| `ExitEffectFloat`       | float                   |
| `ExitEffectGentleFloat` | gentle_float            |
| `ExitEffectZoomIn`      | zoom_in                 |
| `ExitEffectDrop`        | drop                    |
| `ExitEffectSlideLeft`   | slide_left              |
| `ExitEffectSlideRight`  | slide_right             |
| `ExitEffectSlideUp`     | slide_up                |
| `ExitEffectSlideDown`   | slide_down              |
| `ExitEffectPop`         | pop                     |
| `ExitEffectBounce`      | bounce                  |
| `ExitEffectSpin`        | spin                    |
| `ExitEffectSlideBounce` | slide_bounce            |