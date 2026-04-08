# SpeechHistory

## Overview

Accesses your speech history. Your speech history is a list of all your created audio including its metadata using our text-to-speech and speech-to-speech models.

### Available Operations

* [GetSpeechHistory](#getspeechhistory) - List Generated Items
* [GetSpeechHistoryItemByID](#getspeechhistoryitembyid) - Get History Item
* [DeleteSpeechHistoryItem](#deletespeechhistoryitem) - Delete History Item
* [GetAudioFullFromSpeechHistoryItem](#getaudiofullfromspeechhistoryitem) - Get Audio From History Item
* [DownloadSpeechHistoryItems](#downloadspeechhistoryitems) - Download History Items

## GetSpeechHistory

Returns a list of your generated audio.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_speech_history" method="get" path="/v1/history" -->
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

    res, err := s.SpeechHistory.GetSpeechHistory(ctx, operations.GetSpeechHistoryRequest{
        ModelID: elevenlabsgo.Pointer("eleven_turbo_v2"),
        DateBeforeUnix: elevenlabsgo.Pointer[int64](1640995200),
        DateAfterUnix: elevenlabsgo.Pointer[int64](1640995200),
        SortDirection: operations.SortDirectionDesc.ToPointer(),
        Search: elevenlabsgo.Pointer("In the land far far away"),
        Source: operations.SourceTts.ToPointer(),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetSpeechHistoryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `ctx`                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                    | :heavy_check_mark:                                                                       | The context to use for the request.                                                      |
| `request`                                                                                | [operations.GetSpeechHistoryRequest](../../models/operations/getspeechhistoryrequest.md) | :heavy_check_mark:                                                                       | The request object to use for the request.                                               |
| `opts`                                                                                   | [][operations.Option](../../models/operations/option.md)                                 | :heavy_minus_sign:                                                                       | The options for this request.                                                            |

### Response

**[*operations.GetSpeechHistoryResponse](../../models/operations/getspeechhistoryresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSpeechHistoryItemByID

Retrieves a history item.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_speech_history_item_by_id" method="get" path="/v1/history/{history_item_id}" -->
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

    res, err := s.SpeechHistory.GetSpeechHistoryItemByID(ctx, "VW7YKqPnjY4h39yTbx2L")
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeechHistoryItemResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                          | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        | Example                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                              | :heavy_check_mark:                                                                                                                 | The context to use for the request.                                                                                                |                                                                                                                                    |
| `historyItemID`                                                                                                                    | `string`                                                                                                                           | :heavy_check_mark:                                                                                                                 | History item ID to be used, you can use GET https://api.elevenlabs.io/v1/history to receive a list of history items and their IDs. | VW7YKqPnjY4h39yTbx2L                                                                                                               |
| `opts`                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                           | :heavy_minus_sign:                                                                                                                 | The options for this request.                                                                                                      |                                                                                                                                    |

### Response

**[*operations.GetSpeechHistoryItemByIDResponse](../../models/operations/getspeechhistoryitembyidresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteSpeechHistoryItem

Delete a history item by its ID

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_speech_history_item" method="delete" path="/v1/history/{history_item_id}" -->
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

    res, err := s.SpeechHistory.DeleteSpeechHistoryItem(ctx, "VW7YKqPnjY4h39yTbx2L")
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteHistoryItemResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                          | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        | Example                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                              | :heavy_check_mark:                                                                                                                 | The context to use for the request.                                                                                                |                                                                                                                                    |
| `historyItemID`                                                                                                                    | `string`                                                                                                                           | :heavy_check_mark:                                                                                                                 | History item ID to be used, you can use GET https://api.elevenlabs.io/v1/history to receive a list of history items and their IDs. | VW7YKqPnjY4h39yTbx2L                                                                                                               |
| `opts`                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                           | :heavy_minus_sign:                                                                                                                 | The options for this request.                                                                                                      |                                                                                                                                    |

### Response

**[*operations.DeleteSpeechHistoryItemResponse](../../models/operations/deletespeechhistoryitemresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAudioFullFromSpeechHistoryItem

Returns the audio of an history item.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_audio_full_from_speech_history_item" method="get" path="/v1/history/{history_item_id}/audio" -->
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

    res, err := s.SpeechHistory.GetAudioFullFromSpeechHistoryItem(ctx, "VW7YKqPnjY4h39yTbx2L")
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                          | Type                                                                                                                               | Required                                                                                                                           | Description                                                                                                                        | Example                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                              | :heavy_check_mark:                                                                                                                 | The context to use for the request.                                                                                                |                                                                                                                                    |
| `historyItemID`                                                                                                                    | `string`                                                                                                                           | :heavy_check_mark:                                                                                                                 | History item ID to be used, you can use GET https://api.elevenlabs.io/v1/history to receive a list of history items and their IDs. | VW7YKqPnjY4h39yTbx2L                                                                                                               |
| `opts`                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                           | :heavy_minus_sign:                                                                                                                 | The options for this request.                                                                                                      |                                                                                                                                    |

### Response

**[*operations.GetAudioFullFromSpeechHistoryItemResponse](../../models/operations/getaudiofullfromspeechhistoryitemresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DownloadSpeechHistoryItems

Download one or more history items. If one history item ID is provided, we will return a single audio file. If more than one history item IDs are provided, we will provide the history items packed into a .zip file.

### Example Usage

<!-- UsageSnippet language="go" operationID="download_speech_history_items" method="post" path="/v1/history/download" -->
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

    res, err := s.SpeechHistory.DownloadSpeechHistoryItems(ctx, components.BodyDownloadHistoryItemsV1HistoryDownloadPost{
        HistoryItemIds: []string{},
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

| Parameter                                                                                                                            | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                                | :heavy_check_mark:                                                                                                                   | The context to use for the request.                                                                                                  |
| `request`                                                                                                                            | [components.BodyDownloadHistoryItemsV1HistoryDownloadPost](../../models/components/bodydownloadhistoryitemsv1historydownloadpost.md) | :heavy_check_mark:                                                                                                                   | The request object to use for the request.                                                                                           |
| `opts`                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                             | :heavy_minus_sign:                                                                                                                   | The options for this request.                                                                                                        |

### Response

**[*operations.DownloadSpeechHistoryItemsResponse](../../models/operations/downloadspeechhistoryitemsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.BadRequestError     | 400                           | application/json              |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |