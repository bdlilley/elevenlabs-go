# AudioIsolation

## Overview

Isolate speech from background noise in an audio file.

### Available Operations

* [AudioIsolation](#audioisolation) - Audio Isolation
* [GetAudioIsolationHistory](#getaudioisolationhistory) - Get Audio Isolation History
* [DeleteAudioIsolationHistoryItem](#deleteaudioisolationhistoryitem) - Delete Audio Isolation History Item
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

## GetAudioIsolationHistory

Returns a list of all your audio isolation generations.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_audio_isolation_history" method="get" path="/v1/audio-isolation/history" -->
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

    res, err := s.AudioIsolation.GetAudioIsolationHistory(ctx, elevenlabsgo.Pointer[int64](100), elevenlabsgo.Pointer[int64](1), elevenlabsgo.Pointer("podcast"))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAudioIsolationHistoryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     | Example                                                                         |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `ctx`                                                                           | [context.Context](https://pkg.go.dev/context#Context)                           | :heavy_check_mark:                                                              | The context to use for the request.                                             |                                                                                 |
| `pageSize`                                                                      | `*int64`                                                                        | :heavy_minus_sign:                                                              | How many history items to return at maximum. Defaults to 100.                   |                                                                                 |
| `page`                                                                          | `*int64`                                                                        | :heavy_minus_sign:                                                              | Page number for search pagination (1-based). Only used when search is provided. |                                                                                 |
| `search`                                                                        | `*string`                                                                       | :heavy_minus_sign:                                                              | Optional search term used for filtering audio isolation history (title/text).   | **Example 1:** podcast<br/>**Example 2:** lecture                               |
| `opts`                                                                          | [][operations.Option](../../models/operations/option.md)                        | :heavy_minus_sign:                                                              | The options for this request.                                                   |                                                                                 |

### Response

**[*operations.GetAudioIsolationHistoryResponse](../../models/operations/getaudioisolationhistoryresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAudioIsolationHistoryItem

Deletes a specific audio isolation history item and the associated media files.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_audio_isolation_history_item" method="delete" path="/v1/audio-isolation/history/{history_item_id}" -->
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

    res, err := s.AudioIsolation.DeleteAudioIsolationHistoryItem(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `historyItemID`                                          | `string`                                                 | :heavy_check_mark:                                       | Identifier of the audio isolation history item.          |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.DeleteAudioIsolationHistoryItemResponse](../../models/operations/deleteaudioisolationhistoryitemresponse.md), error**

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