# Voices

## Overview

Access to voices created either by you or ElevenLabs.

### Available Operations

* [GetVoices](#getvoices) - List Voices
* [GetUserVoicesV2](#getuservoicesv2) - Get Voices V2
* [GetVoiceSettingsDefault](#getvoicesettingsdefault) - Get Default Voice Settings.
* [GetVoiceSettings](#getvoicesettings) - Get Voice Settings
* [GetVoiceByID](#getvoicebyid) - Get Voice
* [DeleteVoice](#deletevoice) - Delete Voice
* [EditVoiceSettings](#editvoicesettings) - Edit Voice Settings
* [AddVoice](#addvoice) - Add Voice
* [EditVoice](#editvoice) - Edit Voice
* [AddSharingVoice](#addsharingvoice) - Add Shared Voice
* [GetLibraryVoices](#getlibraryvoices) - Get Voices
* [GetSimilarLibraryVoices](#getsimilarlibraryvoices) - Get Similar Library Voices

## GetVoices

Returns a list of all available voices for a user.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_voices" method="get" path="/v1/voices" -->
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

    res, err := s.Voices.GetVoices(ctx, elevenlabsgo.Pointer(true))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetVoicesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         | Example                                                                             |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `ctx`                                                                               | [context.Context](https://pkg.go.dev/context#Context)                               | :heavy_check_mark:                                                                  | The context to use for the request.                                                 |                                                                                     |
| `showLegacy`                                                                        | `*bool`                                                                             | :heavy_minus_sign:                                                                  | If set to true, legacy premade voices will be included in responses from /v1/voices | true                                                                                |
| `opts`                                                                              | [][operations.Option](../../models/operations/option.md)                            | :heavy_minus_sign:                                                                  | The options for this request.                                                       |                                                                                     |

### Response

**[*operations.GetVoicesResponse](../../models/operations/getvoicesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetUserVoicesV2

Gets a list of all available voices for a user with search, filtering and pagination.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_user_voices_v2" method="get" path="/v2/voices" -->
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

    res, err := s.Voices.GetUserVoicesV2(ctx, operations.GetUserVoicesV2Request{
        NextPageToken: elevenlabsgo.Pointer("0"),
        Sort: elevenlabsgo.Pointer("created_at_unix"),
        SortDirection: elevenlabsgo.Pointer("desc"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetVoicesV2ResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                              | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `ctx`                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                  | :heavy_check_mark:                                                                     | The context to use for the request.                                                    |
| `request`                                                                              | [operations.GetUserVoicesV2Request](../../models/operations/getuservoicesv2request.md) | :heavy_check_mark:                                                                     | The request object to use for the request.                                             |
| `opts`                                                                                 | [][operations.Option](../../models/operations/option.md)                               | :heavy_minus_sign:                                                                     | The options for this request.                                                          |

### Response

**[*operations.GetUserVoicesV2Response](../../models/operations/getuservoicesv2response.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetVoiceSettingsDefault

Gets the default settings for voices. "similarity_boost" corresponds to"Clarity + Similarity Enhancement" in the web app and "stability" corresponds to "Stability" slider in the web app.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_voice_settings_default" method="get" path="/v1/voices/settings/default" -->
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

    res, err := s.Voices.GetVoiceSettingsDefault(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.VoiceSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetVoiceSettingsDefaultResponse](../../models/operations/getvoicesettingsdefaultresponse.md), error**

### Errors

| Error Type         | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| apierrors.APIError | 4XX, 5XX           | \*/\*              |

## GetVoiceSettings

Returns the settings for a specific voice. "similarity_boost" corresponds to"Clarity + Similarity Enhancement" in the web app and "stability" corresponds to "Stability" slider in the web app.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_voice_settings" method="get" path="/v1/voices/{voice_id}/settings" -->
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

    res, err := s.Voices.GetVoiceSettings(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.VoiceSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            | Example                                                                                                |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |                                                                                                        |
| `voiceID`                                                                                              | `string`                                                                                               | :heavy_check_mark:                                                                                     | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices. | 21m00Tcm4TlvDq8ikWAM                                                                                   |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |                                                                                                        |

### Response

**[*operations.GetVoiceSettingsResponse](../../models/operations/getvoicesettingsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetVoiceByID

Returns metadata about a specific voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_voice_by_id" method="get" path="/v1/voices/{voice_id}" -->
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

    res, err := s.Voices.GetVoiceByID(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(true))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoiceResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                         | Type                                                                                                                                                                                                              | Required                                                                                                                                                                                                          | Description                                                                                                                                                                                                       | Example                                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                             | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                                                | The context to use for the request.                                                                                                                                                                               |                                                                                                                                                                                                                   |
| `voiceID`                                                                                                                                                                                                         | `string`                                                                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                                                                | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                                                                            | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                              |
| `withSettings`                                                                                                                                                                                                    | `*bool`                                                                                                                                                                                                           | :heavy_minus_sign:                                                                                                                                                                                                | : warning: ** DEPRECATED **: This will be removed in a future release, please migrate away from it as soon as possible.<br/><br/>This parameter is now deprecated. It is ignored and will be removed in a future version. |                                                                                                                                                                                                                   |
| `opts`                                                                                                                                                                                                            | [][operations.Option](../../models/operations/option.md)                                                                                                                                                          | :heavy_minus_sign:                                                                                                                                                                                                | The options for this request.                                                                                                                                                                                     |                                                                                                                                                                                                                   |

### Response

**[*operations.GetVoiceByIDResponse](../../models/operations/getvoicebyidresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteVoice

Deletes a voice by its ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_voice" method="delete" path="/v1/voices/{voice_id}" -->
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

    res, err := s.Voices.DeleteVoice(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteVoiceResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            | Example                                                                                                |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |                                                                                                        |
| `voiceID`                                                                                              | `string`                                                                                               | :heavy_check_mark:                                                                                     | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices. | 21m00Tcm4TlvDq8ikWAM                                                                                   |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |                                                                                                        |

### Response

**[*operations.DeleteVoiceResponse](../../models/operations/deletevoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditVoiceSettings

Edit your settings for a specific voice. "similarity_boost" corresponds to "Clarity + Similarity Enhancement" in the web app and "stability" corresponds to "Stability" slider in the web app.

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_voice_settings" method="post" path="/v1/voices/{voice_id}/settings/edit" -->
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

    res, err := s.Voices.EditVoiceSettings(ctx, "21m00Tcm4TlvDq8ikWAM", components.VoiceSettingsResponseModel{
        Stability: elevenlabsgo.Pointer[float64](1.0),
        UseSpeakerBoost: elevenlabsgo.Pointer(true),
        SimilarityBoost: elevenlabsgo.Pointer[float64](1.0),
        Style: elevenlabsgo.Pointer[float64](0.0),
        Speed: elevenlabsgo.Pointer[float64](1.0),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.EditVoiceSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            | Example                                                                                                |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |                                                                                                        |
| `voiceID`                                                                                              | `string`                                                                                               | :heavy_check_mark:                                                                                     | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices. | 21m00Tcm4TlvDq8ikWAM                                                                                   |
| `body`                                                                                                 | [components.VoiceSettingsResponseModel](../../models/components/voicesettingsresponsemodel.md)         | :heavy_check_mark:                                                                                     | N/A                                                                                                    | {<br/>"similarity_boost": 1,<br/>"speed": 1,<br/>"stability": 1,<br/>"style": 0,<br/>"use_speaker_boost": true<br/>} |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |                                                                                                        |

### Response

**[*operations.EditVoiceSettingsResponse](../../models/operations/editvoicesettingsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddVoice

Add a new voice to your collection of voices in VoiceLab.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_voice" method="post" path="/v1/voices/add" -->
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

    res, err := s.Voices.AddVoice(ctx, components.BodyAddVoiceV1VoicesAddPost{
        Name: "John Smith",
        Files: []components.BodyAddVoiceV1VoicesAddPostFile{},
        RemoveBackgroundNoise: elevenlabsgo.Pointer(true),
        Description: elevenlabsgo.Pointer("An old American male voice with a slight hoarseness in his throat. Perfect for news."),
        Labels: elevenlabsgo.Pointer(components.CreateBodyAddVoiceV1VoicesAddPostLabelsStr(
            "{\"language\": \"en\", \"accent\": \"en-US\", \"gender\": \"male\", \"age\": \"middle-aged\"}",
        )),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddVoiceIVCResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                        | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                            | :heavy_check_mark:                                                                               | The context to use for the request.                                                              |
| `request`                                                                                        | [components.BodyAddVoiceV1VoicesAddPost](../../models/components/bodyaddvoicev1voicesaddpost.md) | :heavy_check_mark:                                                                               | The request object to use for the request.                                                       |
| `opts`                                                                                           | [][operations.Option](../../models/operations/option.md)                                         | :heavy_minus_sign:                                                                               | The options for this request.                                                                    |

### Response

**[*operations.AddVoiceResponse](../../models/operations/addvoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditVoice

Edit a voice created by you.

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_voice" method="post" path="/v1/voices/{voice_id}/edit" -->
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

    res, err := s.Voices.EditVoice(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyEditVoiceV1VoicesVoiceIDEditPost{
        Name: "John Smith",
        RemoveBackgroundNoise: elevenlabsgo.Pointer(true),
        Description: elevenlabsgo.Pointer("An old American male voice with a slight hoarseness in his throat. Perfect for news."),
        Labels: elevenlabsgo.Pointer(components.CreateBodyEditVoiceV1VoicesVoiceIDEditPostLabelsStr(
            "{\"language\": \"en\", \"accent\": \"en-US\", \"gender\": \"male\", \"age\": \"middle-aged\"}",
        )),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.EditVoiceResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                          | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        | Example                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                              | :heavy_check_mark:                                                                                                 | The context to use for the request.                                                                                |                                                                                                                    |
| `voiceID`                                                                                                          | `string`                                                                                                           | :heavy_check_mark:                                                                                                 | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.             | 21m00Tcm4TlvDq8ikWAM                                                                                               |
| `body`                                                                                                             | [components.BodyEditVoiceV1VoicesVoiceIDEditPost](../../models/components/bodyeditvoicev1voicesvoiceideditpost.md) | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |                                                                                                                    |
| `opts`                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                           | :heavy_minus_sign:                                                                                                 | The options for this request.                                                                                      |                                                                                                                    |

### Response

**[*operations.EditVoiceResponse](../../models/operations/editvoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddSharingVoice

Add a shared voice to your collection of voices.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_sharing_voice" method="post" path="/v1/voices/add/{public_user_id}/{voice_id}" -->
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

    res, err := s.Voices.AddSharingVoice(ctx, "63e06b7e7cafdc46be4d2e0b3f045940231ae058d508589653d74d1265a574ca", "21m00Tcm4TlvDq8ikWAM", components.BodyAddSharedVoiceV1VoicesAddPublicUserIDVoiceIDPost{
        NewName: "John Smith",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddVoiceResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                          | Type                                                                                                                                               | Required                                                                                                                                           | Description                                                                                                                                        | Example                                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                                              | :heavy_check_mark:                                                                                                                                 | The context to use for the request.                                                                                                                |                                                                                                                                                    |
| `publicUserID`                                                                                                                                     | `string`                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | Public user ID used to publicly identify ElevenLabs users.                                                                                         | 63e06b7e7cafdc46be4d2e0b3f045940231ae058d508589653d74d1265a574ca                                                                                   |
| `voiceID`                                                                                                                                          | `string`                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                             | 21m00Tcm4TlvDq8ikWAM                                                                                                                               |
| `body`                                                                                                                                             | [components.BodyAddSharedVoiceV1VoicesAddPublicUserIDVoiceIDPost](../../models/components/bodyaddsharedvoicev1voicesaddpublicuseridvoiceidpost.md) | :heavy_check_mark:                                                                                                                                 | N/A                                                                                                                                                |                                                                                                                                                    |
| `opts`                                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                                           | :heavy_minus_sign:                                                                                                                                 | The options for this request.                                                                                                                      |                                                                                                                                                    |

### Response

**[*operations.AddSharingVoiceResponse](../../models/operations/addsharingvoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetLibraryVoices

Retrieves a list of shared voices.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_library_voices" method="get" path="/v1/shared-voices" -->
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

    res, err := s.Voices.GetLibraryVoices(ctx, operations.GetLibraryVoicesRequest{
        Category: operations.CategoryProfessional.ToPointer(),
        Gender: elevenlabsgo.Pointer("male"),
        Age: elevenlabsgo.Pointer("young"),
        Accent: elevenlabsgo.Pointer("american"),
        Language: elevenlabsgo.Pointer("en"),
        Locale: elevenlabsgo.Pointer("en-US"),
        Search: elevenlabsgo.Pointer("tiktok"),
        Featured: elevenlabsgo.Pointer(true),
        MinNoticePeriodDays: elevenlabsgo.Pointer[int64](30),
        IncludeCustomRates: elevenlabsgo.Pointer(true),
        IncludeLiveModerated: elevenlabsgo.Pointer(true),
        ReaderAppEnabled: elevenlabsgo.Pointer(true),
        OwnerID: elevenlabsgo.Pointer("7c9fab611d9a0e1fb2e7448a0c294a8804efc2bcc324b0a366a5d5232b7d1532"),
        Sort: elevenlabsgo.Pointer("created_date"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetLibraryVoicesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `ctx`                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                    | :heavy_check_mark:                                                                       | The context to use for the request.                                                      |
| `request`                                                                                | [operations.GetLibraryVoicesRequest](../../models/operations/getlibraryvoicesrequest.md) | :heavy_check_mark:                                                                       | The request object to use for the request.                                               |
| `opts`                                                                                   | [][operations.Option](../../models/operations/option.md)                                 | :heavy_minus_sign:                                                                       | The options for this request.                                                            |

### Response

**[*operations.GetLibraryVoicesResponse](../../models/operations/getlibraryvoicesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSimilarLibraryVoices

Returns a list of shared voices similar to the provided audio sample. If neither similarity_threshold nor top_k is provided, we will apply default values.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_similar_library_voices" method="post" path="/v1/similar-voices" -->
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

    res, err := s.Voices.GetSimilarLibraryVoices(ctx, &components.BodyGetSimilarLibraryVoicesV1SimilarVoicesPost{
        SimilarityThreshold: elevenlabsgo.Pointer[float64](0.5),
        TopK: elevenlabsgo.Pointer[int64](10),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetLibraryVoicesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                              | Type                                                                                                                                   | Required                                                                                                                               | Description                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                  | :heavy_check_mark:                                                                                                                     | The context to use for the request.                                                                                                    |
| `request`                                                                                                                              | [components.BodyGetSimilarLibraryVoicesV1SimilarVoicesPost](../../models/components/bodygetsimilarlibraryvoicesv1similarvoicespost.md) | :heavy_check_mark:                                                                                                                     | The request object to use for the request.                                                                                             |
| `opts`                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                               | :heavy_minus_sign:                                                                                                                     | The options for this request.                                                                                                          |

### Response

**[*operations.GetSimilarLibraryVoicesResponse](../../models/operations/getsimilarlibraryvoicesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |