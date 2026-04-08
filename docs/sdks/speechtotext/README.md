# SpeechToText

## Overview

Transcribe your audio files with detailed speaker annotations and precise timestamps using our cutting-edge model.

### Available Operations

* [SpeechToText](#speechtotext) - Speech To Text
* [GetTranscriptByID](#gettranscriptbyid) - Get Transcript By Id
* [DeleteTranscriptByID](#deletetranscriptbyid) - Delete Transcript By Id

## SpeechToText

Transcribe an audio or video file. If webhook is set to true, the request will be processed asynchronously and results sent to configured webhooks. When use_multi_channel is true and the provided audio has multiple channels, a 'transcripts' object with separate transcripts for each channel is returned. Otherwise, returns a single transcript. The optional webhook_metadata parameter allows you to attach custom data that will be included in webhook responses for request correlation and tracking.

### Example Usage: multichannel

<!-- UsageSnippet language="go" operationID="speech_to_text" method="post" path="/v1/speech-to-text" example="multichannel" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.SpeechToText.SpeechToText(ctx, components.BodySpeechToTextV1SpeechToTextPost{
        ModelID: components.BodySpeechToTextV1SpeechToTextPostModelIDScribeV2,
        FileFormat: components.BodySpeechToTextV1SpeechToTextPostFileFormatPcmS16le16.ToPointer(),
        SourceURL: optionalnullable.From(elevenlabsgo.Pointer("https://storage.googleapis.com/my-bucket/folder/audio.mp3")),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](12345)),
        WebhookMetadata: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWebhookMetadataStr(
            "{\"user_id\": \"123\", \"session_id\": \"abc-def-ghi\"}",
        ))),
    }, elevenlabsgo.Pointer(true), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseSpeechToTextV1SpeechToTextPost != nil {
        switch res.ResponseSpeechToTextV1SpeechToTextPost.Type {
            case operations.ResponseSpeechToTextV1SpeechToTextPostTypeSpeechToTextChunkResponseModel:
                // res.ResponseSpeechToTextV1SpeechToTextPost.SpeechToTextChunkResponseModel is populated
            case operations.ResponseSpeechToTextV1SpeechToTextPostTypeMultichannelSpeechToTextResponseModel:
                // res.ResponseSpeechToTextV1SpeechToTextPost.MultichannelSpeechToTextResponseModel is populated
            case operations.ResponseSpeechToTextV1SpeechToTextPostTypeSpeechToTextWebhookResponseModel:
                // res.ResponseSpeechToTextV1SpeechToTextPost.SpeechToTextWebhookResponseModel is populated
        }

    }
}
```
### Example Usage: single_channel

<!-- UsageSnippet language="go" operationID="speech_to_text" method="post" path="/v1/speech-to-text" example="single_channel" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.SpeechToText.SpeechToText(ctx, components.BodySpeechToTextV1SpeechToTextPost{
        ModelID: components.BodySpeechToTextV1SpeechToTextPostModelIDScribeV2,
        FileFormat: components.BodySpeechToTextV1SpeechToTextPostFileFormatPcmS16le16.ToPointer(),
        SourceURL: optionalnullable.From(elevenlabsgo.Pointer("https://storage.googleapis.com/my-bucket/folder/audio.mp3")),
        Seed: optionalnullable.From(elevenlabsgo.Pointer[int64](12345)),
        WebhookMetadata: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWebhookMetadataStr(
            "{\"user_id\": \"123\", \"session_id\": \"abc-def-ghi\"}",
        ))),
    }, elevenlabsgo.Pointer(true), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseSpeechToTextV1SpeechToTextPost != nil {
        switch res.ResponseSpeechToTextV1SpeechToTextPost.Type {
            case operations.ResponseSpeechToTextV1SpeechToTextPostTypeSpeechToTextChunkResponseModel:
                // res.ResponseSpeechToTextV1SpeechToTextPost.SpeechToTextChunkResponseModel is populated
            case operations.ResponseSpeechToTextV1SpeechToTextPostTypeMultichannelSpeechToTextResponseModel:
                // res.ResponseSpeechToTextV1SpeechToTextPost.MultichannelSpeechToTextResponseModel is populated
            case operations.ResponseSpeechToTextV1SpeechToTextPostTypeSpeechToTextWebhookResponseModel:
                // res.ResponseSpeechToTextV1SpeechToTextPost.SpeechToTextWebhookResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                | Type                                                                                                                                                                                                                                     | Required                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                                                       | The context to use for the request.                                                                                                                                                                                                      |
| `body`                                                                                                                                                                                                                                   | [components.BodySpeechToTextV1SpeechToTextPost](../../models/components/bodyspeechtotextv1speechtotextpost.md)                                                                                                                           | :heavy_check_mark:                                                                                                                                                                                                                       | N/A                                                                                                                                                                                                                                      |
| `enableLogging`                                                                                                                                                                                                                          | `*bool`                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                       | When enable_logging is set to false zero retention mode will be used for the request. This will mean log and transcript storage features are unavailable for this request. Zero retention mode may only be used by enterprise customers. |
| `xiAPIKey`                                                                                                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                                                                       | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                |
| `opts`                                                                                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                                                                       | The options for this request.                                                                                                                                                                                                            |

### Response

**[*operations.SpeechToTextResponse](../../models/operations/speechtotextresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetTranscriptByID

Retrieve a previously generated transcript by its ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_transcript_by_id" method="get" path="/v1/speech-to-text/transcripts/{transcription_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.SpeechToText.GetTranscriptByID(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetTranscriptByIdv1SpeechToTextTranscriptsTranscriptionIDGet != nil {
        switch res.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGet.Type {
            case operations.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGetTypeSpeechToTextChunkResponseModel:
                // res.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGet.SpeechToTextChunkResponseModel is populated
            case operations.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGetTypeMultichannelSpeechToTextResponseModel:
                // res.ResponseGetTranscriptByIDV1SpeechToTextTranscriptsTranscriptionIDGet.MultichannelSpeechToTextResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `transcriptionID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The unique ID of the transcript to retrieve                                                                                                               |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetTranscriptByIDResponse](../../models/operations/gettranscriptbyidresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteTranscriptByID

Delete a previously generated transcript by its ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_transcript_by_id" method="delete" path="/v1/speech-to-text/transcripts/{transcription_id}" -->
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

    res, err := s.SpeechToText.DeleteTranscriptByID(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `transcriptionID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The unique ID of the transcript to delete                                                                                                                 |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteTranscriptByIDResponse](../../models/operations/deletetranscriptbyidresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |