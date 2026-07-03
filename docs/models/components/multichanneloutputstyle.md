# MultichannelOutputStyle

Controls the response shape when use_multi_channel is enabled. 'separate' (default) returns one transcript per channel under 'transcripts'. 'combined' merges all channels into a single transcript whose words are sorted by start time, each carrying a 'channel_index' - matching the single-channel response shape. 'combined' requires timestamps (timestamps_granularity must not be 'none') and does not support entity detection or redaction.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.MultichannelOutputStyleSeparate
```


## Values

| Name                              | Value                             |
| --------------------------------- | --------------------------------- |
| `MultichannelOutputStyleSeparate` | separate                          |
| `MultichannelOutputStyleCombined` | combined                          |