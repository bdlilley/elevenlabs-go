# TimestampsGranularity

The granularity of the timestamps in the transcription. 'word' provides word-level timestamps and 'character' provides character-level timestamps per word.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.TimestampsGranularityNone
```


## Values

| Name                             | Value                            |
| -------------------------------- | -------------------------------- |
| `TimestampsGranularityNone`      | none                             |
| `TimestampsGranularityWord`      | word                             |
| `TimestampsGranularityCharacter` | character                        |