# Samples

## Overview

Access to your samples. A sample is any audio file you attached to a voice. A voice can have one or more samples.

### Available Operations

* [DeleteSample](#deletesample) - Delete Sample
* [GetAudioFromSample](#getaudiofromsample) - Get Audio From Sample

## DeleteSample

Removes a sample by its ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_sample" method="delete" path="/v1/voices/{voice_id}/samples/{sample_id}" -->
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

    res, err := s.Samples.DeleteSample(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteSampleResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `sampleID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Sample ID to be used, you can use GET https://api.elevenlabs.io/v1/voices/{voice_id} to list all the available samples for a voice.                       | VW7YKqPnjY4h39yTbx2L                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeleteSampleResponse](../../models/operations/deletesampleresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAudioFromSample

Returns the audio corresponding to a sample attached to a voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_audio_from_sample" method="get" path="/v1/voices/{voice_id}/samples/{sample_id}/audio" -->
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

    res, err := s.Samples.GetAudioFromSample(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `sampleID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Sample ID to be used, you can use GET https://api.elevenlabs.io/v1/voices/{voice_id} to list all the available samples for a voice.                       | VW7YKqPnjY4h39yTbx2L                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAudioFromSampleResponse](../../models/operations/getaudiofromsampleresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |