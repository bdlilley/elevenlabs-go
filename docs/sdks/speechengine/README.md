# SpeechEngine

## Overview

Low-latency, real-time speech generation endpoints.

### Available Operations

* [ListSpeechEngines](#listspeechengines) - List Speech Engines
* [CreateSpeechEngine](#createspeechengine) - Create Speech Engine
* [GetSpeechEngine](#getspeechengine) - Get Speech Engine
* [DeleteSpeechEngine](#deletespeechengine) - Delete Speech Engine
* [UpdateSpeechEngine](#updatespeechengine) - Update Speech Engine

## ListSpeechEngines

Returns a paginated list of Speech Engine resources.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_speech_engines" method="get" path="/v1/speech-engine" -->
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

    res, err := s.SpeechEngine.ListSpeechEngines(ctx, operations.ListSpeechEnginesRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.ListSpeechEnginesResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                  | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `ctx`                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                      | :heavy_check_mark:                                                                         | The context to use for the request.                                                        |
| `request`                                                                                  | [operations.ListSpeechEnginesRequest](../../models/operations/listspeechenginesrequest.md) | :heavy_check_mark:                                                                         | The request object to use for the request.                                                 |
| `opts`                                                                                     | [][operations.Option](../../models/operations/option.md)                                   | :heavy_minus_sign:                                                                         | The options for this request.                                                              |

### Response

**[*operations.ListSpeechEnginesResponse](../../models/operations/listspeechenginesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateSpeechEngine

Create a new Speech Engine resource

### Example Usage

<!-- UsageSnippet language="go" operationID="create_speech_engine" method="post" path="/v1/speech-engine" -->
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

    res, err := s.SpeechEngine.CreateSpeechEngine(ctx, components.CreateSpeechEngineRequest{
        SpeechEngine: components.SpeechEngineConfig{
            WsURL: "https://submissive-minority.name/",
        },
        Asr: &components.ASRConversationalConfig{
            Keywords: []string{
                "hello",
                "world",
            },
        },
        Tts: &components.TTSConversationalConfigInput{
            ModelID: components.TTSConversationalModelElevenTurboV2.ToPointer(),
            OptimizeStreamingLatency: components.TTSOptimizeStreamingLatencyThree.ToPointer(),
            PronunciationDictionaryLocators: []components.PydanticPronunciationDictionaryVersionLocator{},
        },
        Turn: &components.BaseTurnConfig{
            InterruptionIgnoreTerms: []string{},
        },
        Conversation: &components.ConversationConfigInput{
            ClientEvents: []components.ClientEvent{
                components.ClientEventAudio,
                components.ClientEventInterruption,
            },
        },
        Privacy: &components.PrivacyConfigInput{},
        CallLimits: &components.AgentCallLimits{},
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeechEngineResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                    | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `ctx`                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                        | :heavy_check_mark:                                                                           | The context to use for the request.                                                          |
| `request`                                                                                    | [components.CreateSpeechEngineRequest](../../models/components/createspeechenginerequest.md) | :heavy_check_mark:                                                                           | The request object to use for the request.                                                   |
| `opts`                                                                                       | [][operations.Option](../../models/operations/option.md)                                     | :heavy_minus_sign:                                                                           | The options for this request.                                                                |

### Response

**[*operations.CreateSpeechEngineResponse](../../models/operations/createspeechengineresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSpeechEngine

Retrieve a Speech Engine resource

### Example Usage

<!-- UsageSnippet language="go" operationID="get_speech_engine" method="get" path="/v1/speech-engine/{speech_engine_id}" -->
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

    res, err := s.SpeechEngine.GetSpeechEngine(ctx, "seng_3701k3ttaq12ewp8b7qv5rfyszkz")
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeechEngineResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `speechEngineID`                                         | `string`                                                 | :heavy_check_mark:                                       | The speech engine ID (accepts seng_ or agent_ prefix)    | seng_3701k3ttaq12ewp8b7qv5rfyszkz                        |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetSpeechEngineResponse](../../models/operations/getspeechengineresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteSpeechEngine

Delete a Speech Engine resource

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_speech_engine" method="delete" path="/v1/speech-engine/{speech_engine_id}" -->
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

    res, err := s.SpeechEngine.DeleteSpeechEngine(ctx, "seng_3701k3ttaq12ewp8b7qv5rfyszkz")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `speechEngineID`                                         | `string`                                                 | :heavy_check_mark:                                       | The speech engine ID (accepts seng_ or agent_ prefix)    | seng_3701k3ttaq12ewp8b7qv5rfyszkz                        |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteSpeechEngineResponse](../../models/operations/deletespeechengineresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSpeechEngine

Update a Speech Engine resource (partial update)

### Example Usage

<!-- UsageSnippet language="go" operationID="update_speech_engine" method="patch" path="/v1/speech-engine/{speech_engine_id}" -->
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

    res, err := s.SpeechEngine.UpdateSpeechEngine(ctx, "seng_3701k3ttaq12ewp8b7qv5rfyszkz", components.UpdateSpeechEngineRequest{
        Asr: &components.ASRConversationalConfig{
            Keywords: []string{
                "hello",
                "world",
            },
        },
        Tts: &components.TTSConversationalConfigInput{
            ModelID: components.TTSConversationalModelElevenTurboV2.ToPointer(),
            OptimizeStreamingLatency: components.TTSOptimizeStreamingLatencyThree.ToPointer(),
            PronunciationDictionaryLocators: []components.PydanticPronunciationDictionaryVersionLocator{},
        },
        Turn: &components.BaseTurnConfig{
            InterruptionIgnoreTerms: []string{},
        },
        Conversation: &components.ConversationConfigInput{
            ClientEvents: []components.ClientEvent{
                components.ClientEventAudio,
                components.ClientEventInterruption,
            },
        },
        Privacy: &components.PrivacyConfigInput{},
        CallLimits: &components.AgentCallLimits{},
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeechEngineResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                    | Type                                                                                         | Required                                                                                     | Description                                                                                  | Example                                                                                      |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `ctx`                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                        | :heavy_check_mark:                                                                           | The context to use for the request.                                                          |                                                                                              |
| `speechEngineID`                                                                             | `string`                                                                                     | :heavy_check_mark:                                                                           | The speech engine ID (accepts seng_ or agent_ prefix)                                        | seng_3701k3ttaq12ewp8b7qv5rfyszkz                                                            |
| `body`                                                                                       | [components.UpdateSpeechEngineRequest](../../models/components/updatespeechenginerequest.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |                                                                                              |
| `opts`                                                                                       | [][operations.Option](../../models/operations/option.md)                                     | :heavy_minus_sign:                                                                           | The options for this request.                                                                |                                                                                              |

### Response

**[*operations.UpdateSpeechEngineResponse](../../models/operations/updatespeechengineresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |