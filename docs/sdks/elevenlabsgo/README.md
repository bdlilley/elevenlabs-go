# ElevenlabsGo SDK

## Overview

ElevenLabs API Documentation: This is the documentation for the ElevenLabs API. You can use this API to use our service programmatically, this is done by using your API key. You can find your API key in the dashboard at https://elevenlabs.io/app/settings/api-keys.

### Available Operations

* [GetUserSubscriptionInfo](#getusersubscriptioninfo) - Get User Subscription Info
* [GetUserInfo](#getuserinfo) - Get User Info
* [UsageCharacters](#usagecharacters) - Get Characters Usage Metrics
* [CreateAgentResponseTest](#createagentresponsetest) - Create Agent Response Test
* [GetAgentResponseTest](#getagentresponsetest) - Get Agent Response Test By Id
* [UpdateAgentResponseTest](#updateagentresponsetest) - Update Agent Response Test
* [DeleteChatResponseTest](#deletechatresponsetest) - Delete Agent Response Test
* [GetAgentResponseTestsSummaries](#getagentresponsetestssummaries) - Get Agent Response Test Summaries By Ids
* [ListChatResponseTests](#listchatresponsetests) - List Agent Response Tests
* [ListTestInvocations](#listtestinvocations) - List Test Invocations
* [RunAgentTestSuite](#runagenttestsuite) - Run Tests On The Agent
* [GetTestInvocation](#gettestinvocation) - Get Test Invocation
* [ResubmitTests](#resubmittests) - Resubmit Tests
* [RedirectToMintlify](#redirecttomintlify) - Redirect To Mintlify

## GetUserSubscriptionInfo

Gets extended information about the users subscription

### Example Usage

<!-- UsageSnippet language="go" operationID="get_user_subscription_info" method="get" path="/v1/user/subscription" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/components"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.GetUserSubscriptionInfo(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.ExtendedSubscriptionResponseModel != nil {
        switch res.ExtendedSubscriptionResponseModel.PendingChange.Type {
            case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
                // res.ExtendedSubscriptionResponseModel.PendingChange.PendingSubscriptionSwitchResponseModel is populated
            case components.PendingChangeTypePendingCancellationResponseModel:
                // res.ExtendedSubscriptionResponseModel.PendingChange.PendingCancellationResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetUserSubscriptionInfoResponse](../../models/operations/getusersubscriptioninforesponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetUserInfo

Gets information about the user

### Example Usage

<!-- UsageSnippet language="go" operationID="get_user_info" method="get" path="/v1/user" -->
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

    res, err := s.GetUserInfo(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.UserResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetUserInfoResponse](../../models/operations/getuserinforesponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UsageCharacters

Returns the usage metrics for the current user or the entire workspace they are part of. The response provides a time axis based on the specified aggregation interval (default: day), with usage values for each interval along that axis. Usage is broken down by the selected breakdown type. For example, breakdown type "voice" will return the usage of each voice for each interval along the time axis.

### Example Usage

<!-- UsageSnippet language="go" operationID="usage_characters" method="get" path="/v1/usage/character-stats" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.UsageCharacters(ctx, operations.UsageCharactersRequest{
        StartUnix: 1685574000,
        EndUnix: 1688165999,
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.UsageCharactersResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                              | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `ctx`                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                  | :heavy_check_mark:                                                                     | The context to use for the request.                                                    |
| `request`                                                                              | [operations.UsageCharactersRequest](../../models/operations/usagecharactersrequest.md) | :heavy_check_mark:                                                                     | The request object to use for the request.                                             |
| `opts`                                                                                 | [][operations.Option](../../models/operations/option.md)                               | :heavy_minus_sign:                                                                     | The options for this request.                                                          |

### Response

**[*operations.UsageCharactersResponse](../../models/operations/usagecharactersresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentResponseTest

Creates a new agent response test.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_response_test_route" method="post" path="/v1/convai/agent-testing/create" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.CreateAgentResponseTest(ctx, operations.CreateCreateAgentResponseTestRouteTestRequestCreateSimulationTestRequest(
        components.CreateSimulationTestRequest{
            Name: "<value>",
        },
    ))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentTestResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `request`                                                                                                                | [operations.CreateAgentResponseTestRouteTestRequest](../../models/operations/createagentresponsetestroutetestrequest.md) | :heavy_check_mark:                                                                                                       | The request object to use for the request.                                                                               |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.CreateAgentResponseTestRouteResponse](../../models/operations/createagentresponsetestrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentResponseTest

Gets an agent response test by ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_response_test_route" method="get" path="/v1/convai/agent-testing/{test_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.GetAgentResponseTest(ctx, "TeaqRRdTcIfIu2i7BYfT")
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetAgentResponseTestByIdv1ConvaiAgentTestingTestIDGet != nil {
        switch res.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGet.Type {
            case operations.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTypeLlm:
                // res.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGet.GetResponseUnitTestResponseModel is populated
            case operations.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTypeTool:
                // res.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGet.GetToolCallUnitTestResponseModel is populated
            case operations.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGetTypeSimulation:
                // res.ResponseGetAgentResponseTestByIDV1ConvaiAgentTestingTestIDGet.GetSimulationTestResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                          | Type                                                               | Required                                                           | Description                                                        | Example                                                            |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `ctx`                                                              | [context.Context](https://pkg.go.dev/context#Context)              | :heavy_check_mark:                                                 | The context to use for the request.                                |                                                                    |
| `testID`                                                           | `string`                                                           | :heavy_check_mark:                                                 | The id of a chat response test. This is returned on test creation. | TeaqRRdTcIfIu2i7BYfT                                               |
| `opts`                                                             | [][operations.Option](../../models/operations/option.md)           | :heavy_minus_sign:                                                 | The options for this request.                                      |                                                                    |

### Response

**[*operations.GetAgentResponseTestRouteResponse](../../models/operations/getagentresponsetestrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateAgentResponseTest

Updates an agent response test by ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_agent_response_test_route" method="put" path="/v1/convai/agent-testing/{test_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.UpdateAgentResponseTest(ctx, "TeaqRRdTcIfIu2i7BYfT", operations.CreateUpdateAgentResponseTestRouteTestRequestUpdateToolCallUnitTestRequest(
        components.UpdateToolCallUnitTestRequest{
            Name: "<value>",
        },
    ))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut != nil {
        switch res.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.Type {
            case operations.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTypeLlm:
                // res.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetResponseUnitTestResponseModel is populated
            case operations.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTypeTool:
                // res.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetToolCallUnitTestResponseModel is populated
            case operations.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPutTypeSimulation:
                // res.ResponseUpdateAgentResponseTestV1ConvaiAgentTestingTestIDPut.GetSimulationTestResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              | Example                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |                                                                                                                          |
| `testID`                                                                                                                 | `string`                                                                                                                 | :heavy_check_mark:                                                                                                       | The id of a chat response test. This is returned on test creation.                                                       | TeaqRRdTcIfIu2i7BYfT                                                                                                     |
| `body`                                                                                                                   | [operations.UpdateAgentResponseTestRouteTestRequest](../../models/operations/updateagentresponsetestroutetestrequest.md) | :heavy_check_mark:                                                                                                       | N/A                                                                                                                      |                                                                                                                          |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |                                                                                                                          |

### Response

**[*operations.UpdateAgentResponseTestRouteResponse](../../models/operations/updateagentresponsetestrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteChatResponseTest

Deletes an agent response test by ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_chat_response_test_route" method="delete" path="/v1/convai/agent-testing/{test_id}" -->
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

    res, err := s.DeleteChatResponseTest(ctx, "TeaqRRdTcIfIu2i7BYfT")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                          | Type                                                               | Required                                                           | Description                                                        | Example                                                            |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `ctx`                                                              | [context.Context](https://pkg.go.dev/context#Context)              | :heavy_check_mark:                                                 | The context to use for the request.                                |                                                                    |
| `testID`                                                           | `string`                                                           | :heavy_check_mark:                                                 | The id of a chat response test. This is returned on test creation. | TeaqRRdTcIfIu2i7BYfT                                               |
| `opts`                                                             | [][operations.Option](../../models/operations/option.md)           | :heavy_minus_sign:                                                 | The options for this request.                                      |                                                                    |

### Response

**[*operations.DeleteChatResponseTestRouteResponse](../../models/operations/deletechatresponsetestrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentResponseTestsSummaries

Gets multiple agent response tests by their IDs. Returns a dictionary mapping test IDs to test summaries.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_response_tests_summaries_route" method="post" path="/v1/convai/agent-testing/summaries" -->
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

    res, err := s.GetAgentResponseTestsSummaries(ctx, components.ListTestsByIdsRequestModel{
        TestIds: []string{
            "test_id_1",
            "test_id_2",
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetTestsSummariesByIdsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                      | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `ctx`                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                          | :heavy_check_mark:                                                                             | The context to use for the request.                                                            |
| `request`                                                                                      | [components.ListTestsByIdsRequestModel](../../models/components/listtestsbyidsrequestmodel.md) | :heavy_check_mark:                                                                             | The request object to use for the request.                                                     |
| `opts`                                                                                         | [][operations.Option](../../models/operations/option.md)                                       | :heavy_minus_sign:                                                                             | The options for this request.                                                                  |

### Response

**[*operations.GetAgentResponseTestsSummariesRouteResponse](../../models/operations/getagentresponsetestssummariesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListChatResponseTests

Lists all agent response tests with pagination support and optional search filtering.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_chat_response_tests_route" method="get" path="/v1/convai/agent-testing" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.ListChatResponseTests(ctx, operations.ListChatResponseTestsRouteRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.GetTestsPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                    | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                        | :heavy_check_mark:                                                                                           | The context to use for the request.                                                                          |
| `request`                                                                                                    | [operations.ListChatResponseTestsRouteRequest](../../models/operations/listchatresponsetestsrouterequest.md) | :heavy_check_mark:                                                                                           | The request object to use for the request.                                                                   |
| `opts`                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                     | :heavy_minus_sign:                                                                                           | The options for this request.                                                                                |

### Response

**[*operations.ListChatResponseTestsRouteResponse](../../models/operations/listchatresponsetestsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListTestInvocations

Lists all test invocations with pagination support and optional search filtering.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_test_invocations_route" method="get" path="/v1/convai/test-invocations" -->
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

    res, err := s.ListTestInvocations(ctx, "<id>", elevenlabsgo.Pointer[int64](30), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetTestInvocationsPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `ctx`                                                                    | [context.Context](https://pkg.go.dev/context#Context)                    | :heavy_check_mark:                                                       | The context to use for the request.                                      |
| `agentID`                                                                | `string`                                                                 | :heavy_check_mark:                                                       | Filter by agent ID                                                       |
| `pageSize`                                                               | `*int64`                                                                 | :heavy_minus_sign:                                                       | How many Tests to return at maximum. Can not exceed 100, defaults to 30. |
| `cursor`                                                                 | `*string`                                                                | :heavy_minus_sign:                                                       | Used for fetching next page. Cursor is returned in the response.         |
| `opts`                                                                   | [][operations.Option](../../models/operations/option.md)                 | :heavy_minus_sign:                                                       | The options for this request.                                            |

### Response

**[*operations.ListTestInvocationsRouteResponse](../../models/operations/listtestinvocationsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RunAgentTestSuite

Run selected tests on the agent with provided configuration. If the agent configuration is provided, it will be used to override default agent configuration.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_agent_test_suite_route" method="post" path="/v1/convai/agents/{agent_id}/run-tests" -->
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

    res, err := s.RunAgentTestSuite(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.RunAgentTestsRequestModel{
        Tests: []components.SingleTestRunRequestModel{},
        AgentConfigOverride: &components.AdhocAgentConfigOverrideForTestRequestModel{
            ConversationConfig: components.ConversationalConfigAPIModelInput{
                Asr: &components.ASRConversationalConfig{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfig{
                    SoftTimeoutConfig: &components.SoftTimeoutConfig{},
                },
                Tts: &components.TTSConversationalConfigInput{
                    ModelID: components.TTSConversationalModelElevenTurboV2.ToPointer(),
                    OptimizeStreamingLatency: components.TTSOptimizeStreamingLatencyThree.ToPointer(),
                    PronunciationDictionaryLocators: []components.PydanticPronunciationDictionaryVersionLocator{},
                },
                Conversation: &components.ConversationConfig{
                    ClientEvents: []components.ClientEvent{
                        components.ClientEventAudio,
                        components.ClientEventInterruption,
                    },
                },
                LanguagePresets: map[string]components.LanguagePresetInput{
                    "key": components.LanguagePresetInput{
                        Overrides: components.ConversationConfigClientOverrideInput{
                            Turn: &components.TurnConfigOverride{
                                SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                                    Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                                },
                            },
                            Tts: &components.TTSConversationalConfigOverride{
                                VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                                Stability: elevenlabsgo.Pointer[float64](0.5),
                                Speed: elevenlabsgo.Pointer[float64](1.0),
                                SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                            },
                            Agent: &components.AgentConfigOverrideInput{
                                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                                Language: elevenlabsgo.Pointer("en"),
                                Prompt: &components.PromptAgentAPIModelOverrideInput{
                                    Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                                    Llm: components.LlmGemini20Flash001.ToPointer(),
                                    ToolIds: []string{},
                                    KnowledgeBase: []components.KnowledgeBaseLocator{},
                                },
                            },
                        },
                    },
                },
                Vad: &components.VADConfig{},
                Agent: &components.AgentConfigAPIModelInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                },
            },
            PlatformSettings: components.AgentPlatformSettingsRequestModel{
                Evaluation: &components.EvaluationSettingsInput{
                    Criteria: []components.PromptEvaluationCriteria{
                        components.PromptEvaluationCriteria{
                            ID: "1234567890",
                            Name: "Customer satisfaction check",
                            ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
                        },
                    },
                },
                Widget: &components.WidgetConfigInput{
                    CustomAvatarPath: elevenlabsgo.Pointer("https://example.com/avatar.png"),
                },
                DataCollection: map[string]components.LiteralJSONSchemaProperty{
                    "key": components.LiteralJSONSchemaProperty{
                        Type: components.LiteralJSONSchemaPropertyTypeString,
                        Description: elevenlabsgo.Pointer("A user-provided message"),
                    },
                },
                Overrides: &components.ConversationInitiationClientDataConfigInput{
                    CustomLlmExtraBody: elevenlabsgo.Pointer(true),
                    EnableConversationInitiationClientDataFromWebhook: elevenlabsgo.Pointer(true),
                },
                WorkspaceOverrides: &components.AgentWorkspaceOverridesInput{
                    ConversationInitiationClientDataWebhook: &components.ConversationInitiationClientDataWebhook{
                        URL: "https://example.com/webhook",
                        RequestHeaders: map[string]components.ConversationInitiationClientDataWebhookRequestHeaders{
                            "Content-Type": components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(
                                "application/json",
                            ),
                        },
                    },
                },
                Testing: &components.AgentTestingSettings{
                    AttachedTests: []components.AttachedTestModel{
                        components.AttachedTestModel{
                            TestID: "test_123",
                            WorkflowNodeID: elevenlabsgo.Pointer("node_abc"),
                        },
                        components.AttachedTestModel{
                            TestID: "test_456",
                        },
                    },
                },
                Auth: &components.AuthSettings{
                    EnableAuth: elevenlabsgo.Pointer(true),
                    Allowlist: []components.AllowlistItem{
                        components.AllowlistItem{
                            Hostname: "https://example.com",
                        },
                    },
                    RequireOriginHeader: elevenlabsgo.Pointer(true),
                    ShareableToken: elevenlabsgo.Pointer("1234567890"),
                },
                CallLimits: &components.AgentCallLimits{},
                Privacy: &components.PrivacyConfigInput{},
            },
            Workflow: &components.AgentWorkflowRequestModel{
                Edges: map[string]components.WorkflowEdgeModelInput{
                    "entry_to_tool_a": components.WorkflowEdgeModelInput{
                        Source: "entry_node",
                        Target: "tool_node_a",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        )),
                    },
                    "start_to_entry": components.WorkflowEdgeModelInput{
                        Source: "start_node",
                        Target: "entry_node",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        )),
                    },
                    "tool_a_to_failure": components.WorkflowEdgeModelInput{
                        Source: "tool_node_a",
                        Target: "failure_node",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        )),
                    },
                    "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                        Source: "tool_node_a",
                        Target: "tool_node_b",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        )),
                    },
                    "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_transfer",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        )),
                    },
                    "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_conversation",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: true,
                            },
                        )),
                    },
                    "tool_b_to_end": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_end",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: true,
                            },
                        )),
                    },
                    "tool_b_to_phone": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_phone",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        )),
                    },
                },
                Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                    "entry_node": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                        components.WorkflowOverrideAgentNodeModelInput{
                            Label: "<value>",
                        },
                    ),
                    "failure_node": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "start_node": components.CreateAgentWorkflowRequestModelNodesEnd(
                        components.WorkflowEndNodeModelInput{},
                    ),
                    "success_conversation": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "success_end": components.CreateAgentWorkflowRequestModelNodesStart(
                        components.WorkflowStartNodeModelInput{},
                    ),
                    "success_phone": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "success_transfer": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                        components.WorkflowPhoneNumberNodeModelInput{
                            TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationSipURIDynamicVariable(
                                components.SIPURIDynamicVariableTransferDestination{
                                    SipURI: "https://feline-subexpression.com/",
                                },
                            ),
                        },
                    ),
                    "tool_node_a": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                        components.WorkflowPhoneNumberNodeModelInput{
                            TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationSipURIDynamicVariable(
                                components.SIPURIDynamicVariableTransferDestination{
                                    SipURI: "https://friendly-futon.com",
                                },
                            ),
                        },
                    ),
                    "tool_node_b": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                        components.WorkflowOverrideAgentNodeModelInput{
                            Label: "<value>",
                        },
                    ),
                },
            },
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetTestSuiteInvocationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                    | Type                                                                                         | Required                                                                                     | Description                                                                                  | Example                                                                                      |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `ctx`                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                        | :heavy_check_mark:                                                                           | The context to use for the request.                                                          |                                                                                              |
| `agentID`                                                                                    | `string`                                                                                     | :heavy_check_mark:                                                                           | The id of an agent. This is returned on agent creation.                                      | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                           |
| `body`                                                                                       | [components.RunAgentTestsRequestModel](../../models/components/runagenttestsrequestmodel.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |                                                                                              |
| `opts`                                                                                       | [][operations.Option](../../models/operations/option.md)                                     | :heavy_minus_sign:                                                                           | The options for this request.                                                                |                                                                                              |

### Response

**[*operations.RunAgentTestSuiteRouteResponse](../../models/operations/runagenttestsuiterouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetTestInvocation

Gets a test invocation by ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_test_invocation_route" method="get" path="/v1/convai/test-invocations/{test_invocation_id}" -->
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

    res, err := s.GetTestInvocation(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetTestSuiteInvocationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                         | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `ctx`                                                             | [context.Context](https://pkg.go.dev/context#Context)             | :heavy_check_mark:                                                | The context to use for the request.                               |
| `testInvocationID`                                                | `string`                                                          | :heavy_check_mark:                                                | The id of a test invocation. This is returned when tests are run. |
| `opts`                                                            | [][operations.Option](../../models/operations/option.md)          | :heavy_minus_sign:                                                | The options for this request.                                     |

### Response

**[*operations.GetTestInvocationRouteResponse](../../models/operations/gettestinvocationrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ResubmitTests

Resubmits specific test runs from a test invocation.

### Example Usage

<!-- UsageSnippet language="go" operationID="resubmit_tests_route" method="post" path="/v1/convai/test-invocations/{test_invocation_id}/resubmit" -->
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

    res, err := s.ResubmitTests(ctx, "<id>", components.ResubmitTestsRequestModel{
        TestRunIds: []string{},
        AgentConfigOverride: &components.AdhocAgentConfigOverrideForTestRequestModel{
            ConversationConfig: components.ConversationalConfigAPIModelInput{
                Asr: &components.ASRConversationalConfig{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfig{
                    SoftTimeoutConfig: &components.SoftTimeoutConfig{},
                },
                Tts: &components.TTSConversationalConfigInput{
                    ModelID: components.TTSConversationalModelElevenTurboV2.ToPointer(),
                    OptimizeStreamingLatency: components.TTSOptimizeStreamingLatencyThree.ToPointer(),
                    PronunciationDictionaryLocators: []components.PydanticPronunciationDictionaryVersionLocator{},
                },
                Conversation: &components.ConversationConfig{
                    ClientEvents: []components.ClientEvent{
                        components.ClientEventAudio,
                        components.ClientEventInterruption,
                    },
                },
                LanguagePresets: map[string]components.LanguagePresetInput{
                    "key": components.LanguagePresetInput{
                        Overrides: components.ConversationConfigClientOverrideInput{
                            Turn: &components.TurnConfigOverride{
                                SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                                    Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                                },
                            },
                            Tts: &components.TTSConversationalConfigOverride{
                                VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                                Stability: elevenlabsgo.Pointer[float64](0.5),
                                Speed: elevenlabsgo.Pointer[float64](1.0),
                                SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                            },
                            Agent: &components.AgentConfigOverrideInput{
                                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                                Language: elevenlabsgo.Pointer("en"),
                                Prompt: &components.PromptAgentAPIModelOverrideInput{
                                    Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                                    Llm: components.LlmGemini20Flash001.ToPointer(),
                                    ToolIds: []string{},
                                    KnowledgeBase: []components.KnowledgeBaseLocator{},
                                },
                            },
                        },
                    },
                },
                Vad: &components.VADConfig{},
                Agent: &components.AgentConfigAPIModelInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                },
            },
            PlatformSettings: components.AgentPlatformSettingsRequestModel{
                Evaluation: &components.EvaluationSettingsInput{
                    Criteria: []components.PromptEvaluationCriteria{
                        components.PromptEvaluationCriteria{
                            ID: "1234567890",
                            Name: "Customer satisfaction check",
                            ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
                        },
                    },
                },
                Widget: &components.WidgetConfigInput{
                    CustomAvatarPath: elevenlabsgo.Pointer("https://example.com/avatar.png"),
                },
                DataCollection: map[string]components.LiteralJSONSchemaProperty{
                    "key": components.LiteralJSONSchemaProperty{
                        Type: components.LiteralJSONSchemaPropertyTypeString,
                        Description: elevenlabsgo.Pointer("A user-provided message"),
                    },
                },
                Overrides: &components.ConversationInitiationClientDataConfigInput{
                    CustomLlmExtraBody: elevenlabsgo.Pointer(true),
                    EnableConversationInitiationClientDataFromWebhook: elevenlabsgo.Pointer(true),
                },
                WorkspaceOverrides: &components.AgentWorkspaceOverridesInput{
                    ConversationInitiationClientDataWebhook: &components.ConversationInitiationClientDataWebhook{
                        URL: "https://example.com/webhook",
                        RequestHeaders: map[string]components.ConversationInitiationClientDataWebhookRequestHeaders{
                            "Content-Type": components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(
                                "application/json",
                            ),
                        },
                    },
                },
                Testing: &components.AgentTestingSettings{
                    AttachedTests: []components.AttachedTestModel{
                        components.AttachedTestModel{
                            TestID: "test_123",
                            WorkflowNodeID: elevenlabsgo.Pointer("node_abc"),
                        },
                        components.AttachedTestModel{
                            TestID: "test_456",
                        },
                    },
                },
                Auth: &components.AuthSettings{
                    EnableAuth: elevenlabsgo.Pointer(true),
                    Allowlist: []components.AllowlistItem{
                        components.AllowlistItem{
                            Hostname: "https://example.com",
                        },
                    },
                    RequireOriginHeader: elevenlabsgo.Pointer(true),
                    ShareableToken: elevenlabsgo.Pointer("1234567890"),
                },
                CallLimits: &components.AgentCallLimits{},
                Privacy: &components.PrivacyConfigInput{},
            },
            Workflow: &components.AgentWorkflowRequestModel{
                Edges: map[string]components.WorkflowEdgeModelInput{
                    "entry_to_tool_a": components.WorkflowEdgeModelInput{
                        Source: "entry_node",
                        Target: "tool_node_a",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: false,
                            },
                        )),
                    },
                    "start_to_entry": components.WorkflowEdgeModelInput{
                        Source: "start_node",
                        Target: "entry_node",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        )),
                    },
                    "tool_a_to_failure": components.WorkflowEdgeModelInput{
                        Source: "tool_node_a",
                        Target: "failure_node",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: false,
                            },
                        )),
                    },
                    "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                        Source: "tool_node_a",
                        Target: "tool_node_b",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                            components.WorkflowExpressionConditionModelInput{
                                Expression: components.CreateASTNodeInputStringLiteral(
                                    components.ASTStringNodeInput{
                                        Value: "<value>",
                                    },
                                ),
                            },
                        )),
                    },
                    "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_transfer",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        )),
                    },
                    "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_conversation",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        )),
                    },
                    "tool_b_to_end": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_end",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                            components.WorkflowExpressionConditionModelInput{
                                Expression: components.CreateASTNodeInputDynamicVariable(
                                    components.ASTDynamicVariableNodeInput{
                                        Name: "<value>",
                                    },
                                ),
                            },
                        )),
                    },
                    "tool_b_to_phone": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_phone",
                        ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: true,
                            },
                        )),
                    },
                },
                Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                    "entry_node": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                        components.WorkflowOverrideAgentNodeModelInput{
                            Label: "<value>",
                        },
                    ),
                    "failure_node": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "start_node": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                        components.WorkflowPhoneNumberNodeModelInput{
                            TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationPhoneDynamicVariable(
                                components.PhoneNumberDynamicVariableTransferDestination{
                                    PhoneNumber: "(481) 491-6122 x22475",
                                },
                            ),
                        },
                    ),
                    "success_conversation": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "success_end": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "success_phone": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                        components.WorkflowOverrideAgentNodeModelInput{
                            Label: "<value>",
                        },
                    ),
                    "success_transfer": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "tool_node_a": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                        components.WorkflowOverrideAgentNodeModelInput{
                            Label: "<value>",
                        },
                    ),
                    "tool_node_b": components.CreateAgentWorkflowRequestModelNodesEnd(
                        components.WorkflowEndNodeModelInput{},
                    ),
                },
            },
        },
        AgentID: "<id>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                    | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `ctx`                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                        | :heavy_check_mark:                                                                           | The context to use for the request.                                                          |
| `testInvocationID`                                                                           | `string`                                                                                     | :heavy_check_mark:                                                                           | The id of a test invocation. This is returned when tests are run.                            |
| `body`                                                                                       | [components.ResubmitTestsRequestModel](../../models/components/resubmittestsrequestmodel.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `opts`                                                                                       | [][operations.Option](../../models/operations/option.md)                                     | :heavy_minus_sign:                                                                           | The options for this request.                                                                |

### Response

**[*operations.ResubmitTestsRouteResponse](../../models/operations/resubmittestsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RedirectToMintlify

Redirect To Mintlify

### Example Usage

<!-- UsageSnippet language="go" operationID="redirect_to_mintlify" method="get" path="/docs" -->
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

    res, err := s.RedirectToMintlify(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.RedirectToMintlifyResponse](../../models/operations/redirecttomintlifyresponse.md), error**

### Errors

| Error Type         | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| apierrors.APIError | 4XX, 5XX           | \*/\*              |