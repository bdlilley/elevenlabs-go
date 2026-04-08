# GetDubbedTranscriptFileFormatType

Format to return transcript in. For subtitles use either 'srt' or 'webvtt', and for a full transcript use 'json'. The 'json' format is not yet supported for Dubbing Studio.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.GetDubbedTranscriptFileFormatTypeSrt
```


## Values

| Name                                      | Value                                     |
| ----------------------------------------- | ----------------------------------------- |
| `GetDubbedTranscriptFileFormatTypeSrt`    | srt                                       |
| `GetDubbedTranscriptFileFormatTypeWebvtt` | webvtt                                    |
| `GetDubbedTranscriptFileFormatTypeJSON`   | json                                      |