# TextToDialogue

## Overview

### Available Operations

* [TextToDialogue](#texttodialogue) - Text To Dialogue (Multi-Voice)
* [TextToDialogueStream](#texttodialoguestream) - Text To Dialogue (Multi-Voice) Streaming
* [TextToDialogueStreamWithTimestamps](#texttodialoguestreamwithtimestamps) - Text To Dialogue Streaming With Timestamps
* [TextToDialogueFullWithTimestamps](#texttodialoguefullwithtimestamps) - Text To Dialogue With Timestamps

## TextToDialogue

Converts a list of text and voice ID pairs into speech (dialogue) and returns audio.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_dialogue" method="post" path="/v1/text-to-dialogue" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToDialogue.TextToDialogue(ctx, components.BodyTextToDialogueMultiVoiceV1TextToDialoguePost{
        Inputs: []components.DialogueInput{
            components.DialogueInput{
                Text: "Hello, how are you?",
                VoiceID: "bYTqZQo3Jz7LQtmGTgwi",
            },
            components.DialogueInput{
                Text: "I'm doing well, thank you!",
                VoiceID: "6lCwbsX1yVjD49QmpkTR",
            },
        },
        Settings: optionalnullable.From(&components.ModelSettingsResponseModel{
            Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
        }),
        PronunciationDictionaryLocators: optionalnullable.From(elevenlabsgo.Pointer([]components.PronunciationDictionaryVersionLocatorRequestModel{
            components.PronunciationDictionaryVersionLocatorRequestModel{
                PronunciationDictionaryID: "test",
                VersionID: optionalnullable.From(elevenlabsgo.Pointer("id2")),
            },
        })),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](12345)),
        ApplyTextNormalization: components.BodyTextToDialogueMultiVoiceV1TextToDialoguePostApplyTextNormalizationOff.ToPointer(),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.BodyTextToDialogueMultiVoiceV1TextToDialoguePost](../../models/components/bodytexttodialoguemultivoicev1texttodialoguepost.md)                                                                                                                                                                                                                                                                                                                                | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*operations.TextToDialogueOutputFormatOfTheGeneratedAudio](../../models/operations/texttodialogueoutputformatofthegeneratedaudio.md)                                                                                                                                                                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM and WAV formats with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.TextToDialogueResponse](../../models/operations/texttodialogueresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToDialogueStream

Converts a list of text and voice ID pairs into speech (dialogue) and returns an audio stream.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_dialogue_stream" method="post" path="/v1/text-to-dialogue/stream" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToDialogue.TextToDialogueStream(ctx, components.BodyTextToDialogueMultiVoiceStreamingV1TextToDialogueStreamPost{
        Inputs: []components.DialogueInput{
            components.DialogueInput{
                Text: "Hello, how are you?",
                VoiceID: "bYTqZQo3Jz7LQtmGTgwi",
            },
            components.DialogueInput{
                Text: "I'm doing well, thank you!",
                VoiceID: "6lCwbsX1yVjD49QmpkTR",
            },
        },
        Settings: optionalnullable.From(&components.ModelSettingsResponseModel{
            Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
        }),
        PronunciationDictionaryLocators: optionalnullable.From(elevenlabsgo.Pointer([]components.PronunciationDictionaryVersionLocatorRequestModel{
            components.PronunciationDictionaryVersionLocatorRequestModel{
                PronunciationDictionaryID: "test",
                VersionID: optionalnullable.From(elevenlabsgo.Pointer("id2")),
            },
        })),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](12345)),
        ApplyTextNormalization: components.BodyTextToDialogueMultiVoiceStreamingV1TextToDialogueStreamPostApplyTextNormalizationOff.ToPointer(),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.BodyTextToDialogueMultiVoiceStreamingV1TextToDialogueStreamPost](../../models/components/bodytexttodialoguemultivoicestreamingv1texttodialoguestreampost.md)                                                                                                                                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.TextToDialogueStreamResponse](../../models/operations/texttodialoguestreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToDialogueStreamWithTimestamps

Converts a list of text and voice ID pairs into speech (dialogue) and returns a stream of JSON blobs containing audio as a base64 encoded string and timestamps

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_dialogue_stream_with_timestamps" method="post" path="/v1/text-to-dialogue/stream/with-timestamps" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToDialogue.TextToDialogueStreamWithTimestamps(ctx, components.BodyTextToDialogueStreamWithTimestamps{
        Inputs: []components.DialogueInput{
            components.DialogueInput{
                Text: "Hello, how are you?",
                VoiceID: "bYTqZQo3Jz7LQtmGTgwi",
            },
            components.DialogueInput{
                Text: "I'm doing well, thank you!",
                VoiceID: "6lCwbsX1yVjD49QmpkTR",
            },
        },
        Settings: optionalnullable.From(&components.ModelSettingsResponseModel{
            Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
        }),
        PronunciationDictionaryLocators: optionalnullable.From(elevenlabsgo.Pointer([]components.PronunciationDictionaryVersionLocatorRequestModel{
            components.PronunciationDictionaryVersionLocatorRequestModel{
                PronunciationDictionaryID: "test",
                VersionID: optionalnullable.From(elevenlabsgo.Pointer("id2")),
            },
        })),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](12345)),
        ApplyTextNormalization: components.BodyTextToDialogueStreamWithTimestampsApplyTextNormalizationOff.ToPointer(),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.StreamingAudioChunkWithTimestampsAndVoiceSegmentsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.BodyTextToDialogueStreamWithTimestamps](../../models/components/bodytexttodialoguestreamwithtimestamps.md)                                                                                                                                                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.TextToDialogueStreamWithTimestampsResponse](../../models/operations/texttodialoguestreamwithtimestampsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToDialogueFullWithTimestamps

Generate dialogue from text with precise character-level timing information for audio-text synchronization.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_dialogue_full_with_timestamps" method="post" path="/v1/text-to-dialogue/with-timestamps" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToDialogue.TextToDialogueFullWithTimestamps(ctx, components.BodyTextToDialogueFullWithTimestamps{
        Inputs: []components.DialogueInput{
            components.DialogueInput{
                Text: "Hello, how are you?",
                VoiceID: "bYTqZQo3Jz7LQtmGTgwi",
            },
            components.DialogueInput{
                Text: "I'm doing well, thank you!",
                VoiceID: "6lCwbsX1yVjD49QmpkTR",
            },
        },
        Settings: optionalnullable.From(&components.ModelSettingsResponseModel{
            Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
        }),
        PronunciationDictionaryLocators: optionalnullable.From(elevenlabsgo.Pointer([]components.PronunciationDictionaryVersionLocatorRequestModel{
            components.PronunciationDictionaryVersionLocatorRequestModel{
                PronunciationDictionaryID: "test",
                VersionID: optionalnullable.From(elevenlabsgo.Pointer("id2")),
            },
        })),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](12345)),
        ApplyTextNormalization: components.BodyTextToDialogueFullWithTimestampsApplyTextNormalizationOff.ToPointer(),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AudioWithTimestampsAndVoiceSegmentsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.BodyTextToDialogueFullWithTimestamps](../../models/components/bodytexttodialoguefullwithtimestamps.md)                                                                                                                                                                                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*operations.TextToDialogueFullWithTimestampsOutputFormatOfTheGeneratedAudio](../../models/operations/texttodialoguefullwithtimestampsoutputformatofthegeneratedaudio.md)                                                                                                                                                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM and WAV formats with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.TextToDialogueFullWithTimestampsResponse](../../models/operations/texttodialoguefullwithtimestampsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |