# RAGIndexStatus

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.RAGIndexStatusNew

// Open enum: custom values can be created with a direct type cast
custom := components.RAGIndexStatus("custom_value")
```


## Values

| Name                              | Value                             |
| --------------------------------- | --------------------------------- |
| `RAGIndexStatusNew`               | new                               |
| `RAGIndexStatusCreated`           | created                           |
| `RAGIndexStatusProcessing`        | processing                        |
| `RAGIndexStatusFailed`            | failed                            |
| `RAGIndexStatusSucceeded`         | succeeded                         |
| `RAGIndexStatusRagLimitExceeded`  | rag_limit_exceeded                |
| `RAGIndexStatusDocumentTooSmall`  | document_too_small                |
| `RAGIndexStatusCannotIndexFolder` | cannot_index_folder               |