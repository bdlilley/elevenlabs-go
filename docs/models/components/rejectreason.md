# RejectReason

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.RejectReasonLacksStructure

// Open enum: custom values can be created with a direct type cast
custom := components.RejectReason("custom_value")
```


## Values

| Name                               | Value                              |
| ---------------------------------- | ---------------------------------- |
| `RejectReasonLacksStructure`       | lacks_structure                    |
| `RejectReasonDoesntOpen`           | doesnt_open                        |
| `RejectReasonNotLiteraryWork`      | not_literary_work                  |
| `RejectReasonLanguageNotSupported` | language_not_supported             |
| `RejectReasonTooShort`             | too_short                          |
| `RejectReasonDuplicate`            | duplicate                          |
| `RejectReasonPromotional`          | promotional                        |
| `RejectReasonFormattingIssues`     | formatting_issues                  |
| `RejectReasonLowQuality`           | low_quality                        |
| `RejectReasonMetadataIncomplete`   | metadata_incomplete                |
| `RejectReasonMetadataInaccurate`   | metadata_inaccurate                |
| `RejectReasonTypos`                | typos                              |
| `RejectReasonReviewError`          | review_error                       |
| `RejectReasonSpam`                 | spam                               |
| `RejectReasonLegalViolation`       | legal_violation                    |
| `RejectReasonContentPolicy`        | content_policy                     |
| `RejectReasonPublicDomain`         | public_domain                      |
| `RejectReasonOther`                | other                              |