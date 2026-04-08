# FilterByCreator

Filters who created the resources being listed, whether it was the user running the request or someone else that shared the resource with them.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

value := operations.FilterByCreatorPersonal
```


## Values

| Name                      | Value                     |
| ------------------------- | ------------------------- |
| `FilterByCreatorPersonal` | personal                  |
| `FilterByCreatorOthers`   | others                    |
| `FilterByCreatorAll`      | all                       |