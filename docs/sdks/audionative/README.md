# AudioNative

## Overview

### Available Operations

* [CreateAudioNativeProject](#createaudionativeproject) - Creates Audio Native Enabled Project.
* [GetAudioNativeProjectSettingsEndpoint](#getaudionativeprojectsettingsendpoint) - Get Audio Native Project Settings
* [AudioNativeProjectUpdateContentEndpoint](#audionativeprojectupdatecontentendpoint) - Update Audio-Native Project Content
* [AudioNativeUpdateContentFromURL](#audionativeupdatecontentfromurl) - Update Audio-Native Content From Url

## CreateAudioNativeProject

Creates Audio Native enabled project, optionally starts conversion and returns project ID and embeddable HTML snippet.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_audio_native_project" method="post" path="/v1/audio-native" -->
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

    res, err := s.AudioNative.CreateAudioNativeProject(ctx, components.BodyCreatesAudioNativeEnabledProjectV1AudioNativePost{
        Name: "<value>",
        PronunciationDictionaryLocators: []string{
            "{\"pronunciation_dictionary_id\": \"21m00Tcm4TlvDq8ikWAM\", \"version_id\": \"BdF0s0aZ3oFoKnDYdTox\"}",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AudioNativeCreateProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyCreatesAudioNativeEnabledProjectV1AudioNativePost](../../models/components/bodycreatesaudionativeenabledprojectv1audionativepost.md)      | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateAudioNativeProjectResponse](../../models/operations/createaudionativeprojectresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAudioNativeProjectSettingsEndpoint

Get player settings for the specific project.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_audio_native_project_settings_endpoint" method="get" path="/v1/audio-native/{project_id}/settings" -->
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

    res, err := s.AudioNative.GetAudioNativeProjectSettingsEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAudioNativeProjectSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `projectID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The ID of the Studio project.                                                                                                                             | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAudioNativeProjectSettingsEndpointResponse](../../models/operations/getaudionativeprojectsettingsendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AudioNativeProjectUpdateContentEndpoint

Updates content for the specific AudioNative Project.

### Example Usage

<!-- UsageSnippet language="go" operationID="audio_native_project_update_content_endpoint" method="post" path="/v1/audio-native/{project_id}/content" -->
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

    res, err := s.AudioNative.AudioNativeProjectUpdateContentEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.AudioNativeEditContentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                           | Type                                                                                                                                                                                | Required                                                                                                                                                                            | Description                                                                                                                                                                         | Example                                                                                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                               | :heavy_check_mark:                                                                                                                                                                  | The context to use for the request.                                                                                                                                                 |                                                                                                                                                                                     |
| `projectID`                                                                                                                                                                         | `string`                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                  | The ID of the Studio project.                                                                                                                                                       | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                |
| `xiAPIKey`                                                                                                                                                                          | optionalnullable.OptionalNullable[`string`]                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                  | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                           |                                                                                                                                                                                     |
| `body`                                                                                                                                                                              | [*components.BodyUpdateAudioNativeProjectContentV1AudioNativeProjectIDContentPost](../../models/components/bodyupdateaudionativeprojectcontentv1audionativeprojectidcontentpost.md) | :heavy_minus_sign:                                                                                                                                                                  | N/A                                                                                                                                                                                 |                                                                                                                                                                                     |
| `opts`                                                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                                                            | :heavy_minus_sign:                                                                                                                                                                  | The options for this request.                                                                                                                                                       |                                                                                                                                                                                     |

### Response

**[*operations.AudioNativeProjectUpdateContentEndpointResponse](../../models/operations/audionativeprojectupdatecontentendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AudioNativeUpdateContentFromURL

Finds an AudioNative project matching the provided URL, extracts content from the URL, updates the project content, and queues it for conversion and auto-publishing.

### Example Usage

<!-- UsageSnippet language="go" operationID="audio_native_update_content_from_url" method="post" path="/v1/audio-native/content" -->
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

    res, err := s.AudioNative.AudioNativeUpdateContentFromURL(ctx, components.BodyUpdateAudioNativeContentFromURLV1AudioNativeContentPost{
        URL: "https://elevenlabs.io/blog/the_first_ai_that_can_laugh/",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AudioNativeEditContentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                        | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                            | :heavy_check_mark:                                                                                                                                               | The context to use for the request.                                                                                                                              |
| `body`                                                                                                                                                           | [components.BodyUpdateAudioNativeContentFromURLV1AudioNativeContentPost](../../models/components/bodyupdateaudionativecontentfromurlv1audionativecontentpost.md) | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `xiAPIKey`                                                                                                                                                       | optionalnullable.OptionalNullable[`string`]                                                                                                                      | :heavy_minus_sign:                                                                                                                                               | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.        |
| `opts`                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                         | :heavy_minus_sign:                                                                                                                                               | The options for this request.                                                                                                                                    |

### Response

**[*operations.AudioNativeUpdateContentFromURLResponse](../../models/operations/audionativeupdatecontentfromurlresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |