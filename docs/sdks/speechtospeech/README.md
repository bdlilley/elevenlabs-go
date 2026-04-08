# SpeechToSpeech

## Overview

Create speech by combining the style and content of an audio file you upload with a voice of your choice.

### Available Operations

* [SpeechToSpeechFull](#speechtospeechfull) - Speech To Speech
* [SpeechToSpeechStream](#speechtospeechstream) - Speech To Speech Streaming

## SpeechToSpeechFull

Transform audio from one voice to another. Maintain full control over emotion, timing and delivery.

### Example Usage

<!-- UsageSnippet language="go" operationID="speech_to_speech_full" method="post" path="/v1/speech-to-speech/{voice_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.SpeechToSpeech.SpeechToSpeechFull(ctx, operations.SpeechToSpeechFullRequest{
        VoiceID: "21m00Tcm4TlvDq8ikWAM",
        Body: components.BodySpeechToSpeechV1SpeechToSpeechVoiceIDPost{
            Audio: components.BodySpeechToSpeechV1SpeechToSpeechVoiceIDPostAudio{
                FileName: "example.file",
                Content: example,
            },
            Seed: elevenlabsgo.Pointer[int64](12345),
            RemoveBackgroundNoise: elevenlabsgo.Pointer(true),
            FileFormat: components.BodySpeechToSpeechV1SpeechToSpeechVoiceIDPostFileFormatPcmS16le16.ToPointer(),
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
| `request`                                                                                    | [operations.SpeechToSpeechFullRequest](../../models/operations/speechtospeechfullrequest.md) | :heavy_check_mark:                                                                           | The request object to use for the request.                                                   |
| `opts`                                                                                       | [][operations.Option](../../models/operations/option.md)                                     | :heavy_minus_sign:                                                                           | The options for this request.                                                                |

### Response

**[*operations.SpeechToSpeechFullResponse](../../models/operations/speechtospeechfullresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SpeechToSpeechStream

Stream audio from one voice to another. Maintain full control over emotion, timing and delivery.

### Example Usage

<!-- UsageSnippet language="go" operationID="speech_to_speech_stream" method="post" path="/v1/speech-to-speech/{voice_id}/stream" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.SpeechToSpeech.SpeechToSpeechStream(ctx, operations.SpeechToSpeechStreamRequest{
        VoiceID: "21m00Tcm4TlvDq8ikWAM",
        Body: components.BodySpeechToSpeechStreamingV1SpeechToSpeechVoiceIDStreamPost{
            Audio: components.BodySpeechToSpeechStreamingV1SpeechToSpeechVoiceIDStreamPostAudio{
                FileName: "example.file",
                Content: example,
            },
            Seed: elevenlabsgo.Pointer[int64](12345),
            RemoveBackgroundNoise: elevenlabsgo.Pointer(true),
            FileFormat: components.BodySpeechToSpeechStreamingV1SpeechToSpeechVoiceIDStreamPostFileFormatPcmS16le16.ToPointer(),
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

| Parameter                                                                                        | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                            | :heavy_check_mark:                                                                               | The context to use for the request.                                                              |
| `request`                                                                                        | [operations.SpeechToSpeechStreamRequest](../../models/operations/speechtospeechstreamrequest.md) | :heavy_check_mark:                                                                               | The request object to use for the request.                                                       |
| `opts`                                                                                           | [][operations.Option](../../models/operations/option.md)                                         | :heavy_minus_sign:                                                                               | The options for this request.                                                                    |

### Response

**[*operations.SpeechToSpeechStreamResponse](../../models/operations/speechtospeechstreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |