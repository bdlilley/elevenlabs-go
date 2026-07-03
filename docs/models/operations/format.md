# Format

Response format. Defaults to 'json'. Set to 'opentelemetry' for an OTLP-compatible trace payload using the same structure as the post-call webhook.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.FormatJSON
```


## Values

| Name                  | Value                 |
| --------------------- | --------------------- |
| `FormatJSON`          | json                  |
| `FormatOpentelemetry` | opentelemetry         |