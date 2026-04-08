# TextToVoice

## Overview

### Available Operations

* [TextToVoice](#texttovoice) - Generate A Voice Preview From Description
* [CreateVoice](#createvoice) - Create A New Voice From Voice Preview
* [TextToVoiceDesign](#texttovoicedesign) - Design A Voice.
* [TextToVoiceRemix](#texttovoiceremix) - Remix A Voice.
* [TextToVoicePreviewStream](#texttovoicepreviewstream) - Text To Voice Preview Streaming

## TextToVoice

Generate a custom voice based on voice description. This method returns a list of voice previews. Each preview has a generated_voice_id and a sample of the voice as base64 encoded mp3 audio. If you like the a voice previewand want to create the voice call /v1/text-to-voice/create-voice-from-preview with the generated_voice_id to create the voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_voice" method="post" path="/v1/text-to-voice/create-previews" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToVoice.TextToVoice(ctx, components.VoicePreviewsRequestModel{
        VoiceDescription: "A sassy squeaky mouse",
        Text: optionalnullable.From(elevenlabsgo.Pointer("Every act of kindness, no matter how small, carries value and can make a difference, as no gesture of goodwill is ever wasted.")),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](11)),
        ShouldEnhance: elevenlabsgo.Pointer(true),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoicePreviewsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.VoicePreviewsRequestModel](../../models/components/voicepreviewsrequestmodel.md)                                                                                                                                                                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.TextToVoiceResponse](../../models/operations/texttovoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateVoice

Create a voice from previously generated voice preview. This endpoint should be called after you fetched a generated_voice_id using POST /v1/text-to-voice/design or POST /v1/text-to-voice/:voice_id/remix.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_voice" method="post" path="/v1/text-to-voice" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToVoice.CreateVoice(ctx, components.BodyCreateANewVoiceFromVoicePreviewV1TextToVoicePost{
        VoiceName: "Sassy squeaky mouse",
        VoiceDescription: "A sassy squeaky mouse",
        GeneratedVoiceID: "37HceQefKmEi3bGovXjL",
        Labels: optionalnullable.From(elevenlabsgo.Pointer(map[string]string{
            "language": "en",
        })),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoiceResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyCreateANewVoiceFromVoicePreviewV1TextToVoicePost](../../models/components/bodycreateanewvoicefromvoicepreviewv1texttovoicepost.md)        | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateVoiceResponse](../../models/operations/createvoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToVoiceDesign

Design a voice via a prompt. This method returns a list of voice previews. Each preview has a generated_voice_id and a sample of the voice as base64 encoded mp3 audio. To create a voice use the generated_voice_id of the preferred preview with the /v1/text-to-voice endpoint.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_voice_design" method="post" path="/v1/text-to-voice/design" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToVoice.TextToVoiceDesign(ctx, components.VoiceDesignRequestModel{
        VoiceDescription: "A sassy squeaky mouse",
        Text: optionalnullable.From(elevenlabsgo.Pointer("Every act of kindness, no matter how small, carries value and can make a difference, as no gesture of goodwill is ever wasted.")),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](11)),
        StreamPreviews: elevenlabsgo.Pointer(true),
        ShouldEnhance: elevenlabsgo.Pointer(true),
        RemixingSessionID: optionalnullable.From(elevenlabsgo.Pointer("123")),
        RemixingSessionIterationID: optionalnullable.From(elevenlabsgo.Pointer("123")),
        Quality: optionalnullable.From(elevenlabsgo.Pointer[float64](0.9)),
        PromptStrength: optionalnullable.From(elevenlabsgo.Pointer[float64](0.25)),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoicePreviewsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.VoiceDesignRequestModel](../../models/components/voicedesignrequestmodel.md)                                                                                                                                                                                                                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.TextToVoiceDesignResponse](../../models/operations/texttovoicedesignresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToVoiceRemix

Remix an existing voice via a prompt. This method returns a list of voice previews. Each preview has a generated_voice_id and a sample of the voice as base64 encoded mp3 audio. To create a voice use the generated_voice_id of the preferred preview with the /v1/text-to-voice endpoint.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_voice_remix" method="post" path="/v1/text-to-voice/{voice_id}/remix" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToVoice.TextToVoiceRemix(ctx, "21m00Tcm4TlvDq8ikWAM", components.VoiceRemixRequestModel{
        VoiceDescription: "Make the voice have a higher pitch.",
        Text: optionalnullable.From(elevenlabsgo.Pointer("Every act of kindness, no matter how small, carries value and can make a difference, as no gesture of goodwill is ever wasted.")),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](11)),
        GuidanceScale: elevenlabsgo.Pointer[float64](5.0),
        StreamPreviews: elevenlabsgo.Pointer(true),
        RemixingSessionID: optionalnullable.From(elevenlabsgo.Pointer("123")),
        RemixingSessionIterationID: optionalnullable.From(elevenlabsgo.Pointer("123")),
        PromptStrength: optionalnullable.From(elevenlabsgo.Pointer[float64](0.25)),
    }, nil, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoicePreviewsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               | Example                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `voiceID`                                                                                                                                                                                                                                                                                                                                                                                                                                                 | `string`                                                                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                                                                                                                                                                                                                                                                                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.VoiceRemixRequestModel](../../models/components/voiceremixrequestmodel.md)                                                                                                                                                                                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

### Response

**[*operations.TextToVoiceRemixResponse](../../models/operations/texttovoiceremixresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextToVoicePreviewStream

Stream a voice preview that was created via the /v1/text-to-voice/design endpoint.

### Example Usage

<!-- UsageSnippet language="go" operationID="text_to_voice_preview_stream" method="get" path="/v1/text-to-voice/{generated_voice_id}/stream" -->
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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.TextToVoice.TextToVoicePreviewStream(ctx, "37HceQefKmEi3bGovXjL", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `generatedVoiceID`                                                                                                                                        | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The generated_voice_id to stream.                                                                                                                         | 37HceQefKmEi3bGovXjL                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.TextToVoicePreviewStreamResponse](../../models/operations/texttovoicepreviewstreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |