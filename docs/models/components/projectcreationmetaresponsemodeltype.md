# ProjectCreationMetaResponseModelType

The type of the project creation action.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ProjectCreationMetaResponseModelTypeBlank

// Open enum: custom values can be created with a direct type cast
custom := components.ProjectCreationMetaResponseModelType("custom_value")
```


## Values

| Name                                                   | Value                                                  |
| ------------------------------------------------------ | ------------------------------------------------------ |
| `ProjectCreationMetaResponseModelTypeBlank`            | blank                                                  |
| `ProjectCreationMetaResponseModelTypeGeneratePodcast`  | generate_podcast                                       |
| `ProjectCreationMetaResponseModelTypeAutoAssignVoices` | auto_assign_voices                                     |
| `ProjectCreationMetaResponseModelTypeDubVideo`         | dub_video                                              |
| `ProjectCreationMetaResponseModelTypeImportSpeech`     | import_speech                                          |