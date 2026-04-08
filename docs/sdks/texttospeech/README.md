# TextToSpeech

## Overview

Convert text into lifelike speech using a voice of your choice.

### Available Operations

* [TextToSpeechFull](#texttospeechfull) - Text To Speech
* [TextToSpeechFullWithTimestamps](#texttospeechfullwithtimestamps) - Text To Speech With Timestamps
* [TextToSpeechStream](#texttospeechstream) - Text To Speech Streaming
* [TextToSpeechStreamWithTimestamps](#texttospeechstreamwithtimestamps) - Text To Speech Streaming With Timestamps

## TextToSpeechFull

Converts text into speech using a voice of your choice and returns audio.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_speech_full" method="post" path="/v1/text-to-speech/{voice_id}" -->
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

    res, err := s.TextToSpeech.TextToSpeechFull(ctx, operations.TextToSpeechFullRequest{
        VoiceID: "21m00Tcm4TlvDq8ikWAM",
        Body: components.BodyTextToSpeechFull{
            Text: "This is a test for the API of ElevenLabs.",
            VoiceSettings: &components.VoiceSettingsResponseModel{
                Stability: elevenlabsgo.Pointer[float64](1.0),
                UseSpeakerBoost: elevenlabsgo.Pointer(true),
                SimilarityBoost: elevenlabsgo.Pointer[float64](1.0),
                Style: elevenlabsgo.Pointer[float64](0.0),
                Speed: elevenlabsgo.Pointer[float64](1.0),
            },
            PronunciationDictionaryLocators: []components.PronunciationDictionaryVersionLocatorRequestModel{
                components.PronunciationDictionaryVersionLocatorRequestModel{
                    PronunciationDictionaryID: "test",
                    VersionID: elevenlabsgo.Pointer("id2"),
                },
            },
            Seed: elevenlabsgo.Pointer[int64](12345),
            PreviousText: elevenlabsgo.Pointer("In the heart of a lush valley surrounded by towering mountains lies the quaint village of Willowbrook."),
            NextText: elevenlabsgo.Pointer("The Willowbrook Festival, held every spring, celebrates the blossoming of the wild bluebells that carpet the nearby forest floors, creating a breathtaking sea of blue under the canopy of fresh green leaves."),
            PreviousRequestIds: []string{
                "09bOJkdYVjKy2oOiiVtR",
                "0p2uKqOnZyce22SPZ9d5",
                "1KYvY8WZAKmcjCJ1mvVB",
            },
            NextRequestIds: []string{
                "3tPgBrD1UdW3snUkGw1K",
                "4D1jAxiRFkolBNUGzXkU",
                "4c8Z4aWliVR2oipYRXhj",
            },
            UsePvcAsIvc: elevenlabsgo.Pointer(true),
            ApplyLanguageTextNormalization: elevenlabsgo.Pointer(true),
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `ctx`                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                    | :heavy_check_mark:                                                                       | The context to use for the request.                                                      |
| `request`                                                                                | [operations.TextToSpeechFullRequest](../../models/operations/texttospeechfullrequest.md) | :heavy_check_mark:                                                                       | The request object to use for the request.                                               |
| `opts`                                                                                   | [][operations.Option](../../models/operations/option.md)                                 | :heavy_minus_sign:                                                                       | The options for this request.                                                            |

### Response

**[*operations.TextToSpeechFullResponse](../../models/operations/texttospeechfullresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToSpeechFullWithTimestamps

Generate speech from text with precise character-level timing information for audio-text synchronization.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_speech_full_with_timestamps" method="post" path="/v1/text-to-speech/{voice_id}/with-timestamps" -->
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

    res, err := s.TextToSpeech.TextToSpeechFullWithTimestamps(ctx, operations.TextToSpeechFullWithTimestampsRequest{
        VoiceID: "21m00Tcm4TlvDq8ikWAM",
        Body: components.BodyTextToSpeechFullWithTimestamps{
            Text: "This is a test for the API of ElevenLabs.",
            VoiceSettings: &components.VoiceSettingsResponseModel{
                Stability: elevenlabsgo.Pointer[float64](1.0),
                UseSpeakerBoost: elevenlabsgo.Pointer(true),
                SimilarityBoost: elevenlabsgo.Pointer[float64](1.0),
                Style: elevenlabsgo.Pointer[float64](0.0),
                Speed: elevenlabsgo.Pointer[float64](1.0),
            },
            PronunciationDictionaryLocators: []components.PronunciationDictionaryVersionLocatorRequestModel{
                components.PronunciationDictionaryVersionLocatorRequestModel{
                    PronunciationDictionaryID: "test",
                    VersionID: elevenlabsgo.Pointer("id2"),
                },
            },
            Seed: elevenlabsgo.Pointer[int64](12345),
            PreviousText: elevenlabsgo.Pointer("In the heart of a lush valley surrounded by towering mountains lies the quaint village of Willowbrook."),
            NextText: elevenlabsgo.Pointer("The Willowbrook Festival, held every spring, celebrates the blossoming of the wild bluebells that carpet the nearby forest floors, creating a breathtaking sea of blue under the canopy of fresh green leaves."),
            PreviousRequestIds: []string{
                "09bOJkdYVjKy2oOiiVtR",
                "0p2uKqOnZyce22SPZ9d5",
                "1KYvY8WZAKmcjCJ1mvVB",
            },
            NextRequestIds: []string{
                "3tPgBrD1UdW3snUkGw1K",
                "4D1jAxiRFkolBNUGzXkU",
                "4c8Z4aWliVR2oipYRXhj",
            },
            UsePvcAsIvc: elevenlabsgo.Pointer(true),
            ApplyTextNormalization: components.BodyTextToSpeechFullWithTimestampsApplyTextNormalizationOn.ToPointer(),
            ApplyLanguageTextNormalization: elevenlabsgo.Pointer(true),
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AudioWithTimestampsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                            | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                | :heavy_check_mark:                                                                                                   | The context to use for the request.                                                                                  |
| `request`                                                                                                            | [operations.TextToSpeechFullWithTimestampsRequest](../../models/operations/texttospeechfullwithtimestampsrequest.md) | :heavy_check_mark:                                                                                                   | The request object to use for the request.                                                                           |
| `opts`                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                             | :heavy_minus_sign:                                                                                                   | The options for this request.                                                                                        |

### Response

**[*operations.TextToSpeechFullWithTimestampsResponse](../../models/operations/texttospeechfullwithtimestampsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToSpeechStream

Converts text into speech using a voice of your choice and returns audio as an audio stream.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_speech_stream" method="post" path="/v1/text-to-speech/{voice_id}/stream" -->
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

    res, err := s.TextToSpeech.TextToSpeechStream(ctx, operations.TextToSpeechStreamRequest{
        VoiceID: "21m00Tcm4TlvDq8ikWAM",
        Body: components.BodyTextToSpeechStream{
            Text: "This is a test for the API of ElevenLabs.",
            VoiceSettings: &components.VoiceSettingsResponseModel{
                Stability: elevenlabsgo.Pointer[float64](1.0),
                UseSpeakerBoost: elevenlabsgo.Pointer(true),
                SimilarityBoost: elevenlabsgo.Pointer[float64](1.0),
                Style: elevenlabsgo.Pointer[float64](0.0),
                Speed: elevenlabsgo.Pointer[float64](1.0),
            },
            PronunciationDictionaryLocators: []components.PronunciationDictionaryVersionLocatorRequestModel{
                components.PronunciationDictionaryVersionLocatorRequestModel{
                    PronunciationDictionaryID: "test",
                    VersionID: elevenlabsgo.Pointer("id2"),
                },
            },
            Seed: elevenlabsgo.Pointer[int64](12345),
            PreviousText: elevenlabsgo.Pointer("In the heart of a lush valley surrounded by towering mountains lies the quaint village of Willowbrook."),
            NextText: elevenlabsgo.Pointer("The Willowbrook Festival, held every spring, celebrates the blossoming of the wild bluebells that carpet the nearby forest floors, creating a breathtaking sea of blue under the canopy of fresh green leaves."),
            PreviousRequestIds: []string{
                "09bOJkdYVjKy2oOiiVtR",
                "0p2uKqOnZyce22SPZ9d5",
                "1KYvY8WZAKmcjCJ1mvVB",
            },
            NextRequestIds: []string{
                "3tPgBrD1UdW3snUkGw1K",
                "4D1jAxiRFkolBNUGzXkU",
                "4c8Z4aWliVR2oipYRXhj",
            },
            UsePvcAsIvc: elevenlabsgo.Pointer(true),
            ApplyTextNormalization: components.BodyTextToSpeechStreamApplyTextNormalizationOff.ToPointer(),
            ApplyLanguageTextNormalization: elevenlabsgo.Pointer(true),
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                    | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `ctx`                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                        | :heavy_check_mark:                                                                           | The context to use for the request.                                                          |
| `request`                                                                                    | [operations.TextToSpeechStreamRequest](../../models/operations/texttospeechstreamrequest.md) | :heavy_check_mark:                                                                           | The request object to use for the request.                                                   |
| `opts`                                                                                       | [][operations.Option](../../models/operations/option.md)                                     | :heavy_minus_sign:                                                                           | The options for this request.                                                                |

### Response

**[*operations.TextToSpeechStreamResponse](../../models/operations/texttospeechstreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToSpeechStreamWithTimestamps

Converts text into speech using a voice of your choice and returns a stream of JSONs containing audio as a base64 encoded string together with information on when which character was spoken.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_speech_stream_with_timestamps" method="post" path="/v1/text-to-speech/{voice_id}/stream/with-timestamps" -->
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

    res, err := s.TextToSpeech.TextToSpeechStreamWithTimestamps(ctx, operations.TextToSpeechStreamWithTimestampsRequest{
        VoiceID: "21m00Tcm4TlvDq8ikWAM",
        Body: components.BodyTextToSpeechStreamWithTimestamps{
            Text: "This is a test for the API of ElevenLabs.",
            VoiceSettings: &components.VoiceSettingsResponseModel{
                Stability: elevenlabsgo.Pointer[float64](1.0),
                UseSpeakerBoost: elevenlabsgo.Pointer(true),
                SimilarityBoost: elevenlabsgo.Pointer[float64](1.0),
                Style: elevenlabsgo.Pointer[float64](0.0),
                Speed: elevenlabsgo.Pointer[float64](1.0),
            },
            PronunciationDictionaryLocators: []components.PronunciationDictionaryVersionLocatorRequestModel{
                components.PronunciationDictionaryVersionLocatorRequestModel{
                    PronunciationDictionaryID: "test",
                    VersionID: elevenlabsgo.Pointer("id2"),
                },
            },
            Seed: elevenlabsgo.Pointer[int64](12345),
            PreviousText: elevenlabsgo.Pointer("In the heart of a lush valley surrounded by towering mountains lies the quaint village of Willowbrook."),
            NextText: elevenlabsgo.Pointer("The Willowbrook Festival, held every spring, celebrates the blossoming of the wild bluebells that carpet the nearby forest floors, creating a breathtaking sea of blue under the canopy of fresh green leaves."),
            PreviousRequestIds: []string{
                "09bOJkdYVjKy2oOiiVtR",
                "0p2uKqOnZyce22SPZ9d5",
                "1KYvY8WZAKmcjCJ1mvVB",
            },
            NextRequestIds: []string{
                "3tPgBrD1UdW3snUkGw1K",
                "4D1jAxiRFkolBNUGzXkU",
                "4c8Z4aWliVR2oipYRXhj",
            },
            UsePvcAsIvc: elevenlabsgo.Pointer(true),
            ApplyTextNormalization: components.BodyTextToSpeechStreamWithTimestampsApplyTextNormalizationOn.ToPointer(),
            ApplyLanguageTextNormalization: elevenlabsgo.Pointer(true),
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.StreamingAudioChunkWithTimestampsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `request`                                                                                                                | [operations.TextToSpeechStreamWithTimestampsRequest](../../models/operations/texttospeechstreamwithtimestampsrequest.md) | :heavy_check_mark:                                                                                                       | The request object to use for the request.                                                                               |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.TextToSpeechStreamWithTimestampsResponse](../../models/operations/texttospeechstreamwithtimestampsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |