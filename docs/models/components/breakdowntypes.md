# BreakdownTypes

How to break down the information. Cannot be "user" or "api_key" if include_workspace_metrics is False.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.BreakdownTypesNone
```


## Values

| Name                                 | Value                                |
| ------------------------------------ | ------------------------------------ |
| `BreakdownTypesNone`                 | none                                 |
| `BreakdownTypesVoice`                | voice                                |
| `BreakdownTypesVoiceMultiplier`      | voice_multiplier                     |
| `BreakdownTypesUser`                 | user                                 |
| `BreakdownTypesGroups`               | groups                               |
| `BreakdownTypesAPIKeys`              | api_keys                             |
| `BreakdownTypesAllAPIKeys`           | all_api_keys                         |
| `BreakdownTypesProductType`          | product_type                         |
| `BreakdownTypesModel`                | model                                |
| `BreakdownTypesResource`             | resource                             |
| `BreakdownTypesRequestQueue`         | request_queue                        |
| `BreakdownTypesRegion`               | region                               |
| `BreakdownTypesSubresourceID`        | subresource_id                       |
| `BreakdownTypesReportingWorkspaceID` | reporting_workspace_id               |
| `BreakdownTypesHasAPIKey`            | has_api_key                          |
| `BreakdownTypesRequestSource`        | request_source                       |