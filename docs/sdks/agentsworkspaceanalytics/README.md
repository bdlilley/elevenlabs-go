# AgentsWorkspaceAnalytics

## Overview

Workspace-level analytics for Conversational AI usage.

### Available Operations

* [RunConversationAnalysis](#runconversationanalysis) - Run Conversation Analysis
* [RunConversationEvaluations](#runconversationevaluations) - Run Conversation Evaluation

## RunConversationAnalysis

Run the analysis for a conversation using the agent's current evaluation criteria and data collection settings.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_analysis" method="post" path="/v1/convai/conversations/{conversation_id}/analysis/run" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsWorkspaceAnalytics.RunConversationAnalysis(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `conversationID`                                         | `string`                                                 | :heavy_check_mark:                                       | ID of the conversation                                   |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.RunConversationAnalysisResponse](../../models/operations/runconversationanalysisresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RunConversationEvaluations

Rerun a specific evaluation for a conversation.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_evaluations" method="post" path="/v1/convai/conversations/{conversation_id}/analysis/evaluations/run" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsWorkspaceAnalytics.RunConversationEvaluations(ctx, "<id>", components.RunConversationEvaluationsRequest{
        EvaluationID: "<id>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                    | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                        | :heavy_check_mark:                                                                                           | The context to use for the request.                                                                          |
| `conversationID`                                                                                             | `string`                                                                                                     | :heavy_check_mark:                                                                                           | ID of the conversation                                                                                       |
| `body`                                                                                                       | [components.RunConversationEvaluationsRequest](../../models/components/runconversationevaluationsrequest.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `opts`                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                     | :heavy_minus_sign:                                                                                           | The options for this request.                                                                                |

### Response

**[*operations.RunConversationEvaluationsResponse](../../models/operations/runconversationevaluationsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |