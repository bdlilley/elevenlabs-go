# AgentsWorkspaceAnalytics

## Overview

### Available Operations

* [RunConversationAnalysis](#runconversationanalysis) - Run Conversation Analysis

## RunConversationAnalysis

Run the analysis for a conversation using the agent's current evaluation criteria and data collection settings.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_analysis" method="post" path="/v1/convai/conversations/{conversation_id}/analysis/run" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsWorkspaceAnalytics.RunConversationAnalysis(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `conversationID`                                                                                                                                          | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the conversation                                                                                                                                    |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.RunConversationAnalysisResponse](../../models/operations/runconversationanalysisresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |