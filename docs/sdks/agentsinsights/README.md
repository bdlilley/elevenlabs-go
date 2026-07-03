# AgentsInsights

## Overview

Query analytics and insights about agent conversations and performance.

### Available Operations

* [GetAgentTopicsRoute](#getagenttopicsroute) - Get Agent Conversation Topics

## GetAgentTopicsRoute

Returns the latest topic discovery run results for a given agent.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_topics_route" method="get" path="/v1/convai/agents/{agent_id}/topics" -->
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

    res, err := s.AgentsInsights.GetAgentTopicsRoute(ctx, "<id>", nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentTopicsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `agentID`                                                                                                                | `string`                                                                                                                 | :heavy_check_mark:                                                                                                       | ID of the agent                                                                                                          |
| `fromUnixSecs`                                                                                                           | `*int64`                                                                                                                 | :heavy_minus_sign:                                                                                                       | Start of the window to view topics for. When set with to_unix_secs, per-day topics in the range are aggregated together. |
| `toUnixSecs`                                                                                                             | `*int64`                                                                                                                 | :heavy_minus_sign:                                                                                                       | End of the window to view topics for.                                                                                    |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.GetAgentTopicsRouteResponse](../../models/operations/getagenttopicsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |