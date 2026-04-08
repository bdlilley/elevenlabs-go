# Enterprise

## Overview

### Available Operations

* [GetDubbingResource](#getdubbingresource) - Get The Dubbing Resource For An Id.
* [AddLanguage](#addlanguage) - Add A Language To The Resource
* [CreateClip](#createclip) - Create A Segment For The Speaker
* [UpdateSegmentLanguage](#updatesegmentlanguage) - Modify A Single Segment
* [MigrateSegments](#migratesegments) - Move Segments Between Speakers
* [DeleteSegment](#deletesegment) - Deletes A Single Segment
* [Transcribe](#transcribe) - Transcribes Segments
* [Translate](#translate) - Translates All Or Some Segments And Languages
* [Dub](#dub) - Dubs All Or Some Segments And Languages
* [UpdateSpeaker](#updatespeaker) - Update Metadata For A Speaker
* [CreateSpeaker](#createspeaker) - Create A New Speaker
* [GetSimilarVoicesForSpeaker](#getsimilarvoicesforspeaker) - Search The Elevenlabs Library For Voices Similar To A Speaker.
* [Render](#render) - Render Audio Or Video For The Given Language

## GetDubbingResource

Given a dubbing ID generated from the '/v1/dubbing' endpoint with studio enabled, returns the dubbing resource.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_dubbing_resource" method="get" path="/v1/dubbing/resource/{dubbing_id}" -->
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

    res, err := s.Enterprise.GetDubbingResource(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.DubbingResource != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `dubbingID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the dubbing project.                                                                                                                                |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetDubbingResourceResponse](../../models/operations/getdubbingresourceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddLanguage

Adds the given ElevenLab Turbo V2/V2.5 language code to the resource. Does not automatically generate transcripts/translations/audio.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_language" method="post" path="/v1/dubbing/resource/{dubbing_id}/language" -->
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
    )

    res, err := s.Enterprise.AddLanguage(ctx, "<id>", components.BodyAddALanguageToTheResourceV1DubbingResourceDubbingIDLanguagePost{
        Language: nil,
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.LanguageAddedResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                        | Type                                                                                                                                                                             | Required                                                                                                                                                                         | Description                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                            | :heavy_check_mark:                                                                                                                                                               | The context to use for the request.                                                                                                                                              |
| `dubbingID`                                                                                                                                                                      | `string`                                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                               | ID of the dubbing project.                                                                                                                                                       |
| `body`                                                                                                                                                                           | [components.BodyAddALanguageToTheResourceV1DubbingResourceDubbingIDLanguagePost](../../models/components/bodyaddalanguagetotheresourcev1dubbingresourcedubbingidlanguagepost.md) | :heavy_check_mark:                                                                                                                                                               | N/A                                                                                                                                                                              |
| `xiAPIKey`                                                                                                                                                                       | optionalnullable.OptionalNullable[`string`]                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                               | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                        |
| `opts`                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                         | :heavy_minus_sign:                                                                                                                                                               | The options for this request.                                                                                                                                                    |

### Response

**[*operations.AddLanguageResponse](../../models/operations/addlanguageresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateClip

Creates a new segment in dubbing resource with a start and end time for the speaker in every available language. Does not automatically generate transcripts/translations/audio.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_clip" method="post" path="/v1/dubbing/resource/{dubbing_id}/speaker/{speaker_id}/segment" -->
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
    )

    res, err := s.Enterprise.CreateClip(ctx, "<id>", "<id>", components.SegmentCreatePayload{
        StartTime: 4694.58,
        EndTime: 6710.18,
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentCreateResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `dubbingID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the dubbing project.                                                                                                                                |
| `speakerID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the speaker.                                                                                                                                        |
| `body`                                                                                                                                                    | [components.SegmentCreatePayload](../../models/components/segmentcreatepayload.md)                                                                        | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateClipResponse](../../models/operations/createclipresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSegmentLanguage

Modifies a single segment with new text and/or start/end times. Will update the values for only a specific language of a segment. Does not automatically regenerate the dub.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_segment_language" method="patch" path="/v1/dubbing/resource/{dubbing_id}/segment/{segment_id}/{language}" -->
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
        "https://api.example.com",
    )

    res, err := s.Enterprise.UpdateSegmentLanguage(ctx, operations.UpdateSegmentLanguageRequest{
        DubbingID: "<id>",
        SegmentID: "<id>",
        Language: "<value>",
        Body: components.SegmentUpdatePayload{},
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentUpdateResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                          | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                              | :heavy_check_mark:                                                                                 | The context to use for the request.                                                                |
| `request`                                                                                          | [operations.UpdateSegmentLanguageRequest](../../models/operations/updatesegmentlanguagerequest.md) | :heavy_check_mark:                                                                                 | The request object to use for the request.                                                         |
| `opts`                                                                                             | [][operations.Option](../../models/operations/option.md)                                           | :heavy_minus_sign:                                                                                 | The options for this request.                                                                      |

### Response

**[*operations.UpdateSegmentLanguageResponse](../../models/operations/updatesegmentlanguageresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## MigrateSegments

Change the attribution of one or more segments to a different speaker.

### Example Usage

<!-- UsageSnippet language="go" operationID="migrate_segments" method="post" path="/v1/dubbing/resource/{dubbing_id}/migrate-segments" -->
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
    )

    res, err := s.Enterprise.MigrateSegments(ctx, "<id>", components.BodyMoveSegmentsBetweenSpeakersV1DubbingResourceDubbingIDMigrateSegmentsPost{
        SegmentIds: []string{
            "<value 1>",
            "<value 2>",
            "<value 3>",
        },
        SpeakerID: "<id>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentMigrationResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                          | Type                                                                                                                                                                                               | Required                                                                                                                                                                                           | Description                                                                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                 | The context to use for the request.                                                                                                                                                                |
| `dubbingID`                                                                                                                                                                                        | `string`                                                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                                                 | ID of the dubbing project.                                                                                                                                                                         |
| `body`                                                                                                                                                                                             | [components.BodyMoveSegmentsBetweenSpeakersV1DubbingResourceDubbingIDMigrateSegmentsPost](../../models/components/bodymovesegmentsbetweenspeakersv1dubbingresourcedubbingidmigratesegmentspost.md) | :heavy_check_mark:                                                                                                                                                                                 | N/A                                                                                                                                                                                                |
| `xiAPIKey`                                                                                                                                                                                         | optionalnullable.OptionalNullable[`string`]                                                                                                                                                        | :heavy_minus_sign:                                                                                                                                                                                 | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                          |
| `opts`                                                                                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                                                                                           | :heavy_minus_sign:                                                                                                                                                                                 | The options for this request.                                                                                                                                                                      |

### Response

**[*operations.MigrateSegmentsResponse](../../models/operations/migratesegmentsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteSegment

Deletes a single segment from the dubbing.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_segment" method="delete" path="/v1/dubbing/resource/{dubbing_id}/segment/{segment_id}" -->
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

    res, err := s.Enterprise.DeleteSegment(ctx, "<id>", "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentDeleteResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `dubbingID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the dubbing project.                                                                                                                                |
| `segmentID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the segment                                                                                                                                         |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteSegmentResponse](../../models/operations/deletesegmentresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## Transcribe

Regenerate the transcriptions for the specified segments. Does not automatically regenerate translations or dubs.

### Example Usage

<!-- UsageSnippet language="go" operationID="transcribe" method="post" path="/v1/dubbing/resource/{dubbing_id}/transcribe" -->
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
    )

    res, err := s.Enterprise.Transcribe(ctx, "<id>", components.BodyTranscribesSegmentsV1DubbingResourceDubbingIDTranscribePost{
        Segments: []string{
            "<value 1>",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentTranscriptionResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                | Type                                                                                                                                                                     | Required                                                                                                                                                                 | Description                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                    | :heavy_check_mark:                                                                                                                                                       | The context to use for the request.                                                                                                                                      |
| `dubbingID`                                                                                                                                                              | `string`                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                       | ID of the dubbing project.                                                                                                                                               |
| `body`                                                                                                                                                                   | [components.BodyTranscribesSegmentsV1DubbingResourceDubbingIDTranscribePost](../../models/components/bodytranscribessegmentsv1dubbingresourcedubbingidtranscribepost.md) | :heavy_check_mark:                                                                                                                                                       | N/A                                                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                                              | :heavy_minus_sign:                                                                                                                                                       | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                |
| `opts`                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                 | :heavy_minus_sign:                                                                                                                                                       | The options for this request.                                                                                                                                            |

### Response

**[*operations.TranscribeResponse](../../models/operations/transcriberesponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## Translate

Regenerate the translations for either the entire resource or the specified segments/languages. Will automatically transcribe missing transcriptions. Will not automatically regenerate the dubs.

### Example Usage

<!-- UsageSnippet language="go" operationID="translate" method="post" path="/v1/dubbing/resource/{dubbing_id}/translate" -->
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
    )

    res, err := s.Enterprise.Translate(ctx, "<id>", components.BodyTranslatesAllOrSomeSegmentsAndLanguagesV1DubbingResourceDubbingIDTranslatePost{
        Segments: []string{
            "<value 1>",
            "<value 2>",
        },
        Languages: []string{
            "<value 1>",
            "<value 2>",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentTranslationResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                      | Type                                                                                                                                                                                                           | Required                                                                                                                                                                                                       | Description                                                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                                                             | The context to use for the request.                                                                                                                                                                            |
| `dubbingID`                                                                                                                                                                                                    | `string`                                                                                                                                                                                                       | :heavy_check_mark:                                                                                                                                                                                             | ID of the dubbing project.                                                                                                                                                                                     |
| `body`                                                                                                                                                                                                         | [components.BodyTranslatesAllOrSomeSegmentsAndLanguagesV1DubbingResourceDubbingIDTranslatePost](../../models/components/bodytranslatesallorsomesegmentsandlanguagesv1dubbingresourcedubbingidtranslatepost.md) | :heavy_check_mark:                                                                                                                                                                                             | N/A                                                                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                                                                     | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                                                             | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                      |
| `opts`                                                                                                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                             | The options for this request.                                                                                                                                                                                  |

### Response

**[*operations.TranslateResponse](../../models/operations/translateresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## Dub

Regenerate the dubs for either the entire resource or the specified segments/languages. Will automatically transcribe and translate any missing transcriptions and translations.

### Example Usage

<!-- UsageSnippet language="go" operationID="dub" method="post" path="/v1/dubbing/resource/{dubbing_id}/dub" -->
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
    )

    res, err := s.Enterprise.Dub(ctx, "<id>", components.BodyDubsAllOrSomeSegmentsAndLanguagesV1DubbingResourceDubbingIDDubPost{
        Segments: []string{},
        Languages: []string{
            "<value 1>",
            "<value 2>",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SegmentDubResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                              | Type                                                                                                                                                                                   | Required                                                                                                                                                                               | Description                                                                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                     | The context to use for the request.                                                                                                                                                    |
| `dubbingID`                                                                                                                                                                            | `string`                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                     | ID of the dubbing project.                                                                                                                                                             |
| `body`                                                                                                                                                                                 | [components.BodyDubsAllOrSomeSegmentsAndLanguagesV1DubbingResourceDubbingIDDubPost](../../models/components/bodydubsallorsomesegmentsandlanguagesv1dubbingresourcedubbingiddubpost.md) | :heavy_check_mark:                                                                                                                                                                     | N/A                                                                                                                                                                                    |
| `xiAPIKey`                                                                                                                                                                             | optionalnullable.OptionalNullable[`string`]                                                                                                                                            | :heavy_minus_sign:                                                                                                                                                                     | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                              |
| `opts`                                                                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                     | The options for this request.                                                                                                                                                          |

### Response

**[*operations.DubResponse](../../models/operations/dubresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSpeaker

Amend the metadata associated with a speaker, such as their voice. Both voice cloning and using voices from the ElevenLabs library are supported.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_speaker" method="patch" path="/v1/dubbing/resource/{dubbing_id}/speaker/{speaker_id}" -->
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

    res, err := s.Enterprise.UpdateSpeaker(ctx, "<id>", "<id>", optionalnullable.From[string](nil), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeakerUpdatedResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                           | Type                                                                                                                                                                                                | Required                                                                                                                                                                                            | Description                                                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                                  | The context to use for the request.                                                                                                                                                                 |
| `dubbingID`                                                                                                                                                                                         | `string`                                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                  | ID of the dubbing project.                                                                                                                                                                          |
| `speakerID`                                                                                                                                                                                         | `string`                                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                  | ID of the speaker.                                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                                                          | optionalnullable.OptionalNullable[`string`]                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                  | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                           |
| `body`                                                                                                                                                                                              | [*components.BodyUpdateMetadataForASpeakerV1DubbingResourceDubbingIDSpeakerSpeakerIDPatch](../../models/components/bodyupdatemetadataforaspeakerv1dubbingresourcedubbingidspeakerspeakeridpatch.md) | :heavy_minus_sign:                                                                                                                                                                                  | N/A                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                                                                            | :heavy_minus_sign:                                                                                                                                                                                  | The options for this request.                                                                                                                                                                       |

### Response

**[*operations.UpdateSpeakerResponse](../../models/operations/updatespeakerresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateSpeaker

Create A New Speaker

### Example Usage

<!-- UsageSnippet language="go" operationID="create_speaker" method="post" path="/v1/dubbing/resource/{dubbing_id}/speaker" -->
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

    res, err := s.Enterprise.CreateSpeaker(ctx, "<id>", optionalnullable.From[string](nil), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeakerCreatedResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                       | Type                                                                                                                                                            | Required                                                                                                                                                        | Description                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                           | [context.Context](https://pkg.go.dev/context#Context)                                                                                                           | :heavy_check_mark:                                                                                                                                              | The context to use for the request.                                                                                                                             |
| `dubbingID`                                                                                                                                                     | `string`                                                                                                                                                        | :heavy_check_mark:                                                                                                                                              | ID of the dubbing project.                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                      | optionalnullable.OptionalNullable[`string`]                                                                                                                     | :heavy_minus_sign:                                                                                                                                              | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.       |
| `body`                                                                                                                                                          | [*components.BodyCreateANewSpeakerV1DubbingResourceDubbingIDSpeakerPost](../../models/components/bodycreateanewspeakerv1dubbingresourcedubbingidspeakerpost.md) | :heavy_minus_sign:                                                                                                                                              | N/A                                                                                                                                                             |
| `opts`                                                                                                                                                          | [][operations.Option](../../models/operations/option.md)                                                                                                        | :heavy_minus_sign:                                                                                                                                              | The options for this request.                                                                                                                                   |

### Response

**[*operations.CreateSpeakerResponse](../../models/operations/createspeakerresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSimilarVoicesForSpeaker

Fetch the top 10 similar voices to a speaker, including the voice IDs, names, descriptions, and, where possible, a sample audio recording.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_similar_voices_for_speaker" method="get" path="/v1/dubbing/resource/{dubbing_id}/speaker/{speaker_id}/similar-voices" -->
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

    res, err := s.Enterprise.GetSimilarVoicesForSpeaker(ctx, "<id>", "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SimilarVoicesForSpeakerResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `dubbingID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the dubbing project.                                                                                                                                |
| `speakerID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the speaker.                                                                                                                                        |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetSimilarVoicesForSpeakerResponse](../../models/operations/getsimilarvoicesforspeakerresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## Render

Regenerate the output media for a language using the latest Studio state. Please ensure all segments have been dubbed before rendering, otherwise they will be omitted. Renders are generated asynchronously, and to check the status of all renders please use the 'Get Dubbing Resource' endpoint.

### Example Usage

<!-- UsageSnippet language="go" operationID="render" method="post" path="/v1/dubbing/resource/{dubbing_id}/render/{language}" -->
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
    )

    res, err := s.Enterprise.Render(ctx, "<id>", "<value>", components.BodyRenderAudioOrVideoForTheGivenLanguageV1DubbingResourceDubbingIDRenderLanguagePost{
        RenderType: components.RenderTypeMp3,
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.DubbingRenderResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                            | Type                                                                                                                                                                                                                 | Required                                                                                                                                                                                                             | Description                                                                                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                | :heavy_check_mark:                                                                                                                                                                                                   | The context to use for the request.                                                                                                                                                                                  |
| `dubbingID`                                                                                                                                                                                                          | `string`                                                                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                                                   | ID of the dubbing project.                                                                                                                                                                                           |
| `language`                                                                                                                                                                                                           | `string`                                                                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                                                   | The target language code to render, eg. 'es'. To render the source track use 'original'.                                                                                                                             |
| `body`                                                                                                                                                                                                               | [components.BodyRenderAudioOrVideoForTheGivenLanguageV1DubbingResourceDubbingIDRenderLanguagePost](../../models/components/bodyrenderaudioorvideoforthegivenlanguagev1dubbingresourcedubbingidrenderlanguagepost.md) | :heavy_check_mark:                                                                                                                                                                                                   | N/A                                                                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                                                                           | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                          | :heavy_minus_sign:                                                                                                                                                                                                   | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                            |
| `opts`                                                                                                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                                                                                                             | :heavy_minus_sign:                                                                                                                                                                                                   | The options for this request.                                                                                                                                                                                        |

### Response

**[*operations.RenderResponse](../../models/operations/renderresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |