# AudioIsolation

## Overview

### Available Operations

* [AudioIsolation](#audioisolation) - Audio Isolation
* [AudioIsolationStream](#audioisolationstream) - Audio Isolation Stream

## AudioIsolation

Removes background noise from audio

### Example Usage

<!-- UsageSnippet language="go" operationID="audio_isolation" method="post" path="/v1/audio-isolation" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
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

    res, err := s.AudioIsolation.AudioIsolation(ctx, components.BodyAudioIsolationV1AudioIsolationPost{
        Audio: components.BodyAudioIsolationV1AudioIsolationPostAudio{
            FileName: "example.file",
            Content: example,
        },
        FileFormat: components.BodyAudioIsolationV1AudioIsolationPostFileFormatPcmS16le16.ToPointer(),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                              | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                  | :heavy_check_mark:                                                                                                     | The context to use for the request.                                                                                    |
| `request`                                                                                                              | [components.BodyAudioIsolationV1AudioIsolationPost](../../models/components/bodyaudioisolationv1audioisolationpost.md) | :heavy_check_mark:                                                                                                     | The request object to use for the request.                                                                             |
| `opts`                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                               | :heavy_minus_sign:                                                                                                     | The options for this request.                                                                                          |

### Response

**[*operations.AudioIsolationResponse](../../models/operations/audioisolationresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AudioIsolationStream

Removes background noise from audio and streams the result

### Example Usage

<!-- UsageSnippet language="go" operationID="audio_isolation_stream" method="post" path="/v1/audio-isolation/stream" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
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

    res, err := s.AudioIsolation.AudioIsolationStream(ctx, components.BodyAudioIsolationStreamV1AudioIsolationStreamPost{
        Audio: components.BodyAudioIsolationStreamV1AudioIsolationStreamPostAudio{
            FileName: "example.file",
            Content: example,
        },
        FileFormat: components.BodyAudioIsolationStreamV1AudioIsolationStreamPostFileFormatPcmS16le16.ToPointer(),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                      | Type                                                                                                                                           | Required                                                                                                                                       | Description                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                                          | :heavy_check_mark:                                                                                                                             | The context to use for the request.                                                                                                            |
| `request`                                                                                                                                      | [components.BodyAudioIsolationStreamV1AudioIsolationStreamPost](../../models/components/bodyaudioisolationstreamv1audioisolationstreampost.md) | :heavy_check_mark:                                                                                                                             | The request object to use for the request.                                                                                                     |
| `opts`                                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                                       | :heavy_minus_sign:                                                                                                                             | The options for this request.                                                                                                                  |

### Response

**[*operations.AudioIsolationStreamResponse](../../models/operations/audioisolationstreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |