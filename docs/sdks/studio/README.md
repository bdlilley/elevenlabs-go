# Studio

## Overview

### Available Operations

* [CreatePodcast](#createpodcast) - Create Podcast
* [UpdatePronunciationDictionaries](#updatepronunciationdictionaries) - Create Pronunciation Dictionaries
* [GetProjects](#getprojects) - List Studio Projects
* [AddProject](#addproject) - Create Studio Project
* [GetProjectByID](#getprojectbyid) - Get Studio Project
* [EditProject](#editproject) - Update Studio Project
* [DeleteProject](#deleteproject) - Delete Studio Project
* [EditProjectContent](#editprojectcontent) - Update Studio Project Content
* [ConvertProjectEndpoint](#convertprojectendpoint) - Convert Studio Project
* [GetProjectSnapshots](#getprojectsnapshots) - List Studio Project Snapshots
* [GetProjectSnapshotEndpoint](#getprojectsnapshotendpoint) - Get Project Snapshot
* [StreamProjectSnapshotAudioEndpoint](#streamprojectsnapshotaudioendpoint) - Stream Studio Project Audio
* [StreamProjectSnapshotArchiveEndpoint](#streamprojectsnapshotarchiveendpoint) - Stream Archive With Studio Project Audio
* [GetChapters](#getchapters) - List Chapters
* [AddChapter](#addchapter) - Create Chapter
* [GetChapterByIDEndpoint](#getchapterbyidendpoint) - Get Chapter
* [EditChapter](#editchapter) - Update Chapter
* [DeleteChapterEndpoint](#deletechapterendpoint) - Delete Chapter
* [ConvertChapterEndpoint](#convertchapterendpoint) - Convert Chapter
* [GetChapterSnapshots](#getchaptersnapshots) - List Chapter Snapshots
* [GetChapterSnapshotEndpoint](#getchaptersnapshotendpoint) - Get Chapter Snapshot
* [StreamChapterSnapshotAudio](#streamchaptersnapshotaudio) - Stream Chapter Audio
* [GetProjectMutedTracksEndpoint](#getprojectmutedtracksendpoint) - Get Project Muted Tracks

## CreatePodcast

Create and auto-convert a podcast project. Currently, the LLM cost is covered by us but you will still be charged for the audio generation. In the future, you will be charged for both the LLM and audio generation costs.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_podcast" method="post" path="/v1/studio/podcasts" -->
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

    res, err := s.Studio.CreatePodcast(ctx, components.BodyCreatePodcastV1StudioPodcastsPost{
        ModelID: "eleven_multilingual_v2",
        Mode: components.CreateModeConversation(
            components.PodcastConversationMode{
                Conversation: components.PodcastConversationModeData{
                    HostVoiceID: "6lCwbsX1yVjD49QmpkTR",
                    GuestVoiceID: "bYTqZQo3Jz7LQtmGTgwi",
                },
            },
        ),
        Source: components.CreateSourceUnion2PodcastURLSource(
            components.PodcastURLSource{
                URL: "https://en.wikipedia.org/wiki/Cognitive_science",
            },
        ),
        DurationScale: components.TheDurationOfTheGeneratedPodcastThisVariesDependingOnTheFormatVoiceAndLanguageShort.ToPointer(),
        Language: elevenlabsgo.Pointer("en"),
        Intro: elevenlabsgo.Pointer("Welcome to the podcast."),
        Outro: elevenlabsgo.Pointer("Thank you for listening!"),
        InstructionsPrompt: elevenlabsgo.Pointer("Ensure the podcast remains factual, accurate and appropriate for all audiences."),
        Highlights: []string{
            "Emphasize the importance of AI on education",
        },
    }, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.PodcastProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                            | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                | :heavy_check_mark:                                                                                                   | The context to use for the request.                                                                                  |
| `body`                                                                                                               | [components.BodyCreatePodcastV1StudioPodcastsPost](../../models/components/bodycreatepodcastv1studiopodcastspost.md) | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `safetyIdentifier`                                                                                                   | `*string`                                                                                                            | :heavy_minus_sign:                                                                                                   | Used for moderation. Your workspace must be allowlisted to use this feature.                                         |
| `opts`                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                             | :heavy_minus_sign:                                                                                                   | The options for this request.                                                                                        |

### Response

**[*operations.CreatePodcastResponse](../../models/operations/createpodcastresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdatePronunciationDictionaries

Create a set of pronunciation dictionaries acting on a project. This will automatically mark text within this project as requiring reconverting where the new dictionary would apply or the old one no longer does.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_pronunciation_dictionaries" method="post" path="/v1/studio/projects/{project_id}/pronunciation-dictionaries" -->
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

    res, err := s.Studio.UpdatePronunciationDictionaries(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyCreatePronunciationDictionariesV1StudioProjectsProjectIDPronunciationDictionariesPost{
        PronunciationDictionaryLocators: []components.PronunciationDictionaryVersionLocatorDBModel{
            components.PronunciationDictionaryVersionLocatorDBModel{
                PronunciationDictionaryID: "21m00Tcm4TlvDq8ikWAM",
                VersionID: elevenlabsgo.Pointer("BdF0s0aZ3oFoKnDYdTox"),
            },
        },
        InvalidateAffectedText: elevenlabsgo.Pointer(false),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.CreatePronunciationDictionaryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                    | Type                                                                                                                                                                                                                         | Required                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                  | Example                                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                                                           | The context to use for the request.                                                                                                                                                                                          |                                                                                                                                                                                                                              |
| `projectID`                                                                                                                                                                                                                  | `string`                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                           | The ID of the Studio project.                                                                                                                                                                                                | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                         |
| `body`                                                                                                                                                                                                                       | [components.BodyCreatePronunciationDictionariesV1StudioProjectsProjectIDPronunciationDictionariesPost](../../models/components/bodycreatepronunciationdictionariesv1studioprojectsprojectidpronunciationdictionariespost.md) | :heavy_check_mark:                                                                                                                                                                                                           | N/A                                                                                                                                                                                                                          |                                                                                                                                                                                                                              |
| `opts`                                                                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                                           | The options for this request.                                                                                                                                                                                                |                                                                                                                                                                                                                              |

### Response

**[*operations.UpdatePronunciationDictionariesResponse](../../models/operations/updatepronunciationdictionariesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetProjects

Returns a list of your Studio projects with metadata.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_projects" method="get" path="/v1/studio/projects" -->
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

    res, err := s.Studio.GetProjects(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetProjectsResponseModel != nil {
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

**[*operations.GetProjectsResponse](../../models/operations/getprojectsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddProject

Creates a new Studio project, it can be either initialized as blank, from a document or from a URL.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_project" method="post" path="/v1/studio/projects" -->
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

    res, err := s.Studio.AddProject(ctx, components.BodyCreateStudioProjectV1StudioProjectsPost{
        Name: "Project 1",
        DefaultTitleVoiceID: elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"),
        DefaultParagraphVoiceID: elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"),
        DefaultModelID: elevenlabsgo.Pointer("eleven_multilingual_v2"),
        FromURL: elevenlabsgo.Pointer("https://blog.elevenlabs.io/the_first_ai_that_can_laugh/"),
        FromContentJSON: elevenlabsgo.Pointer("[{\"name\": \"Chapter A\", \"blocks\": [{\"sub_type\": \"p\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"A\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"B\", \"type\": \"tts_node\"}]}, {\"sub_type\": \"h1\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"C\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"D\", \"type\": \"tts_node\"}]}]}, {\"name\": \"Chapter B\", \"blocks\": [{\"sub_type\": \"p\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"E\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"F\", \"type\": \"tts_node\"}]}, {\"sub_type\": \"h2\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"G\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"H\", \"type\": \"tts_node\"}]}]}]"),
        Title: elevenlabsgo.Pointer("Romeo and Juliet"),
        Author: elevenlabsgo.Pointer("William Shakespeare"),
        Description: elevenlabsgo.Pointer("A tragic love story between two young lovers."),
        Genres: []string{
            "Romance",
            "Drama",
        },
        TargetAudience: components.BodyCreateStudioProjectV1StudioProjectsPostTargetAudienceAdult.ToPointer(),
        Language: elevenlabsgo.Pointer("en"),
        ContentType: elevenlabsgo.Pointer("Book"),
        OriginalPublicationDate: elevenlabsgo.Pointer("1597-01-01"),
        MatureContent: elevenlabsgo.Pointer(false),
        IsbnNumber: elevenlabsgo.Pointer("0-306-40615-2"),
        PronunciationDictionaryLocators: []string{
            "{\"pronunciation_dictionary_id\": \"21m00Tcm4TlvDq8ikWAM\", \"version_id\": \"BdF0s0aZ3oFoKnDYdTox\"}",
        },
        Fiction: components.BodyCreateStudioProjectV1StudioProjectsPostFictionFiction.ToPointer(),
        SourceType: components.BodyCreateStudioProjectV1StudioProjectsPostSourceTypeBook.ToPointer(),
        VoiceSettings: []string{
            "{\"voice_id\": \"21m00Tcm4TlvDq8ikWAM\", \"stability\": 0.7, \"similarity_boost\": 0.8, \"style\": 0.5, \"speed\": 1.0, \"use_speaker_boost\": true}",
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                        | Type                                                                                                                             | Required                                                                                                                         | Description                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                            | :heavy_check_mark:                                                                                                               | The context to use for the request.                                                                                              |
| `request`                                                                                                                        | [components.BodyCreateStudioProjectV1StudioProjectsPost](../../models/components/bodycreatestudioprojectv1studioprojectspost.md) | :heavy_check_mark:                                                                                                               | The request object to use for the request.                                                                                       |
| `opts`                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                         | :heavy_minus_sign:                                                                                                               | The options for this request.                                                                                                    |

### Response

**[*operations.AddProjectResponse](../../models/operations/addprojectresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetProjectByID

Returns information about a specific Studio project. This endpoint returns more detailed information about a project than `GET /v1/studio`.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_project_by_id" method="get" path="/v1/studio/projects/{project_id}" -->
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

    res, err := s.Studio.GetProjectByID(ctx, "21m00Tcm4TlvDq8ikWAM", nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ProjectExtendedResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `shareID`                                                | `*string`                                                | :heavy_minus_sign:                                       | The share ID of the project                              |                                                          |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetProjectByIDResponse](../../models/operations/getprojectbyidresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditProject

Updates the specified Studio project by setting the values of the parameters passed.

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_project" method="post" path="/v1/studio/projects/{project_id}" -->
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

    res, err := s.Studio.EditProject(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyUpdateStudioProjectV1StudioProjectsProjectIDPost{
        Name: "Project 1",
        DefaultTitleVoiceID: "21m00Tcm4TlvDq8ikWAM",
        DefaultParagraphVoiceID: "21m00Tcm4TlvDq8ikWAM",
        Title: elevenlabsgo.Pointer("Romeo and Juliet"),
        Author: elevenlabsgo.Pointer("William Shakespeare"),
        IsbnNumber: elevenlabsgo.Pointer("0-306-40615-2"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.EditProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                          | Type                                                                                                                                               | Required                                                                                                                                           | Description                                                                                                                                        | Example                                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                                              | :heavy_check_mark:                                                                                                                                 | The context to use for the request.                                                                                                                |                                                                                                                                                    |
| `projectID`                                                                                                                                        | `string`                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | The ID of the Studio project.                                                                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                               |
| `body`                                                                                                                                             | [components.BodyUpdateStudioProjectV1StudioProjectsProjectIDPost](../../models/components/bodyupdatestudioprojectv1studioprojectsprojectidpost.md) | :heavy_check_mark:                                                                                                                                 | N/A                                                                                                                                                |                                                                                                                                                    |
| `opts`                                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                                           | :heavy_minus_sign:                                                                                                                                 | The options for this request.                                                                                                                      |                                                                                                                                                    |

### Response

**[*operations.EditProjectResponse](../../models/operations/editprojectresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteProject

Deletes a Studio project.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_project" method="delete" path="/v1/studio/projects/{project_id}" -->
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

    res, err := s.Studio.DeleteProject(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteProjectResponse](../../models/operations/deleteprojectresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditProjectContent

Updates Studio project content.

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_project_content" method="post" path="/v1/studio/projects/{project_id}/content" -->
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

    res, err := s.Studio.EditProjectContent(ctx, "21m00Tcm4TlvDq8ikWAM", &components.BodyUpdateStudioProjectContentV1StudioProjectsProjectIDContentPost{
        FromURL: elevenlabsgo.Pointer("https://blog.elevenlabs.io/the_first_ai_that_can_laugh/"),
        FromContentJSON: elevenlabsgo.Pointer("[{\"name\": \"Chapter A\", \"blocks\": [{\"sub_type\": \"p\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"A\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"B\", \"type\": \"tts_node\"}]}, {\"sub_type\": \"h1\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"C\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"D\", \"type\": \"tts_node\"}]}]}, {\"name\": \"Chapter B\", \"blocks\": [{\"sub_type\": \"p\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"E\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"F\", \"type\": \"tts_node\"}]}, {\"sub_type\": \"h2\", \"nodes\": [{\"voice_id\": \"6lCwbsX1yVjD49QmpkT0\", \"text\": \"G\", \"type\": \"tts_node\"}, {\"voice_id\": \"6lCwbsX1yVjD49QmpkT1\", \"text\": \"H\", \"type\": \"tts_node\"}]}]}]"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.EditProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                       | Type                                                                                                                                                                            | Required                                                                                                                                                                        | Description                                                                                                                                                                     | Example                                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                           | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                           | :heavy_check_mark:                                                                                                                                                              | The context to use for the request.                                                                                                                                             |                                                                                                                                                                                 |
| `projectID`                                                                                                                                                                     | `string`                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                              | The ID of the Studio project.                                                                                                                                                   | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                            |
| `body`                                                                                                                                                                          | [*components.BodyUpdateStudioProjectContentV1StudioProjectsProjectIDContentPost](../../models/components/bodyupdatestudioprojectcontentv1studioprojectsprojectidcontentpost.md) | :heavy_minus_sign:                                                                                                                                                              | N/A                                                                                                                                                                             |                                                                                                                                                                                 |
| `opts`                                                                                                                                                                          | [][operations.Option](../../models/operations/option.md)                                                                                                                        | :heavy_minus_sign:                                                                                                                                                              | The options for this request.                                                                                                                                                   |                                                                                                                                                                                 |

### Response

**[*operations.EditProjectContentResponse](../../models/operations/editprojectcontentresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ConvertProjectEndpoint

Starts conversion of a Studio project and all of its chapters.

### Example Usage

<!-- UsageSnippet language="go" operationID="convert_project_endpoint" method="post" path="/v1/studio/projects/{project_id}/convert" -->
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

    res, err := s.Studio.ConvertProjectEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ConvertProjectResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.ConvertProjectEndpointResponse](../../models/operations/convertprojectendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetProjectSnapshots

Retrieves a list of snapshots for a Studio project.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_project_snapshots" method="get" path="/v1/studio/projects/{project_id}/snapshots" -->
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

    res, err := s.Studio.GetProjectSnapshots(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ProjectSnapshotsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetProjectSnapshotsResponse](../../models/operations/getprojectsnapshotsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetProjectSnapshotEndpoint

Returns the project snapshot.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_project_snapshot_endpoint" method="get" path="/v1/studio/projects/{project_id}/snapshots/{project_snapshot_id}" -->
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

    res, err := s.Studio.GetProjectSnapshotEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ProjectSnapshotExtendedResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `projectSnapshotID`                                      | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project snapshot.                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetProjectSnapshotEndpointResponse](../../models/operations/getprojectsnapshotendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## StreamProjectSnapshotAudioEndpoint

Stream the audio from a Studio project snapshot.

### Example Usage

<!-- UsageSnippet language="go" operationID="stream_project_snapshot_audio_endpoint" method="post" path="/v1/studio/projects/{project_id}/snapshots/{project_snapshot_id}/stream" -->
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

    res, err := s.Studio.StreamProjectSnapshotAudioEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM", nil)
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                     | Type                                                                                                                                                                                                                          | Required                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                   | Example                                                                                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                         | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                                                                            | The context to use for the request.                                                                                                                                                                                           |                                                                                                                                                                                                                               |
| `projectID`                                                                                                                                                                                                                   | `string`                                                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                            | The ID of the Studio project.                                                                                                                                                                                                 | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                          |
| `projectSnapshotID`                                                                                                                                                                                                           | `string`                                                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                            | The ID of the Studio project snapshot.                                                                                                                                                                                        | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                          |
| `body`                                                                                                                                                                                                                        | [*components.BodyStreamStudioProjectAudioV1StudioProjectsProjectIDSnapshotsProjectSnapshotIDStreamPost](../../models/components/bodystreamstudioprojectaudiov1studioprojectsprojectidsnapshotsprojectsnapshotidstreampost.md) | :heavy_minus_sign:                                                                                                                                                                                                            | N/A                                                                                                                                                                                                                           |                                                                                                                                                                                                                               |
| `opts`                                                                                                                                                                                                                        | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                                                                            | The options for this request.                                                                                                                                                                                                 |                                                                                                                                                                                                                               |

### Response

**[*operations.StreamProjectSnapshotAudioEndpointResponse](../../models/operations/streamprojectsnapshotaudioendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## StreamProjectSnapshotArchiveEndpoint

Returns a compressed archive of the Studio project's audio.

### Example Usage

<!-- UsageSnippet language="go" operationID="stream_project_snapshot_archive_endpoint" method="post" path="/v1/studio/projects/{project_id}/snapshots/{project_snapshot_id}/archive" -->
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

    res, err := s.Studio.StreamProjectSnapshotArchiveEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `projectSnapshotID`                                      | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project snapshot.                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.StreamProjectSnapshotArchiveEndpointResponse](../../models/operations/streamprojectsnapshotarchiveendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetChapters

Returns a list of a Studio project's chapters.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_chapters" method="get" path="/v1/studio/projects/{project_id}/chapters" -->
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

    res, err := s.Studio.GetChapters(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetChaptersResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetChaptersResponse](../../models/operations/getchaptersresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddChapter

Creates a new chapter either as blank or from a URL.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_chapter" method="post" path="/v1/studio/projects/{project_id}/chapters" -->
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

    res, err := s.Studio.AddChapter(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyCreateChapterV1StudioProjectsProjectIDChaptersPost{
        Name: "Chapter 1",
        FromURL: elevenlabsgo.Pointer("https://blog.elevenlabs.io/the_first_ai_that_can_laugh/"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddChapterResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                              | Type                                                                                                                                                   | Required                                                                                                                                               | Description                                                                                                                                            | Example                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                                  | :heavy_check_mark:                                                                                                                                     | The context to use for the request.                                                                                                                    |                                                                                                                                                        |
| `projectID`                                                                                                                                            | `string`                                                                                                                                               | :heavy_check_mark:                                                                                                                                     | The ID of the Studio project.                                                                                                                          | 21m00Tcm4TlvDq8ikWAM                                                                                                                                   |
| `body`                                                                                                                                                 | [components.BodyCreateChapterV1StudioProjectsProjectIDChaptersPost](../../models/components/bodycreatechapterv1studioprojectsprojectidchapterspost.md) | :heavy_check_mark:                                                                                                                                     | N/A                                                                                                                                                    |                                                                                                                                                        |
| `opts`                                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                                               | :heavy_minus_sign:                                                                                                                                     | The options for this request.                                                                                                                          |                                                                                                                                                        |

### Response

**[*operations.AddChapterResponse](../../models/operations/addchapterresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetChapterByIDEndpoint

Returns information about a specific chapter.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_chapter_by_id_endpoint" method="get" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}" -->
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

    res, err := s.Studio.GetChapterByIDEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ChapterWithContentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `chapterID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the chapter.                                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetChapterByIDEndpointResponse](../../models/operations/getchapterbyidendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditChapter

Updates a chapter.

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_chapter" method="post" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}" -->
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

    res, err := s.Studio.EditChapter(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM", &components.BodyUpdateChapterV1StudioProjectsProjectIDChaptersChapterIDPost{
        Name: elevenlabsgo.Pointer("Chapter 1"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.EditChapterResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                 | Type                                                                                                                                                                      | Required                                                                                                                                                                  | Description                                                                                                                                                               | Example                                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                     | :heavy_check_mark:                                                                                                                                                        | The context to use for the request.                                                                                                                                       |                                                                                                                                                                           |
| `projectID`                                                                                                                                                               | `string`                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | The ID of the Studio project.                                                                                                                                             | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                      |
| `chapterID`                                                                                                                                                               | `string`                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | The ID of the chapter.                                                                                                                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                      |
| `body`                                                                                                                                                                    | [*components.BodyUpdateChapterV1StudioProjectsProjectIDChaptersChapterIDPost](../../models/components/bodyupdatechapterv1studioprojectsprojectidchapterschapteridpost.md) | :heavy_minus_sign:                                                                                                                                                        | N/A                                                                                                                                                                       |                                                                                                                                                                           |
| `opts`                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                  | :heavy_minus_sign:                                                                                                                                                        | The options for this request.                                                                                                                                             |                                                                                                                                                                           |

### Response

**[*operations.EditChapterResponse](../../models/operations/editchapterresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteChapterEndpoint

Deletes a chapter.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_chapter_endpoint" method="delete" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}" -->
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

    res, err := s.Studio.DeleteChapterEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteChapterResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `chapterID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the chapter.                                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteChapterEndpointResponse](../../models/operations/deletechapterendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ConvertChapterEndpoint

Starts conversion of a specific chapter.

### Example Usage

<!-- UsageSnippet language="go" operationID="convert_chapter_endpoint" method="post" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}/convert" -->
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

    res, err := s.Studio.ConvertChapterEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ConvertChapterResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `chapterID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the chapter.                                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.ConvertChapterEndpointResponse](../../models/operations/convertchapterendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetChapterSnapshots

Gets information about all the snapshots of a chapter. Each snapshot can be downloaded as audio. Whenever a chapter is converted a snapshot will automatically be created.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_chapter_snapshots" method="get" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}/snapshots" -->
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

    res, err := s.Studio.GetChapterSnapshots(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ChapterSnapshotsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `chapterID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the chapter.                                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetChapterSnapshotsResponse](../../models/operations/getchaptersnapshotsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetChapterSnapshotEndpoint

Returns the chapter snapshot.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_chapter_snapshot_endpoint" method="get" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}/snapshots/{chapter_snapshot_id}" -->
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

    res, err := s.Studio.GetChapterSnapshotEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ChapterSnapshotExtendedResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `chapterID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the chapter.                                   | 21m00Tcm4TlvDq8ikWAM                                     |
| `chapterSnapshotID`                                      | `string`                                                 | :heavy_check_mark:                                       | The ID of the chapter snapshot.                          | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetChapterSnapshotEndpointResponse](../../models/operations/getchaptersnapshotendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## StreamChapterSnapshotAudio

Stream the audio from a chapter snapshot. Use `GET /v1/studio/projects/{project_id}/chapters/{chapter_id}/snapshots` to return the snapshots of a chapter.

### Example Usage

<!-- UsageSnippet language="go" operationID="stream_chapter_snapshot_audio" method="post" path="/v1/studio/projects/{project_id}/chapters/{chapter_id}/snapshots/{chapter_snapshot_id}/stream" -->
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

    res, err := s.Studio.StreamChapterSnapshotAudio(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM", nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                           | Type                                                                                                                                                                                                                                                | Required                                                                                                                                                                                                                                            | Description                                                                                                                                                                                                                                         | Example                                                                                                                                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                                                                                  | The context to use for the request.                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                     |
| `projectID`                                                                                                                                                                                                                                         | `string`                                                                                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                                                  | The ID of the Studio project.                                                                                                                                                                                                                       | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                |
| `chapterID`                                                                                                                                                                                                                                         | `string`                                                                                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                                                  | The ID of the chapter.                                                                                                                                                                                                                              | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                |
| `chapterSnapshotID`                                                                                                                                                                                                                                 | `string`                                                                                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                                                  | The ID of the chapter snapshot.                                                                                                                                                                                                                     | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                |
| `body`                                                                                                                                                                                                                                              | [*components.BodyStreamChapterAudioV1StudioProjectsProjectIDChaptersChapterIDSnapshotsChapterSnapshotIDStreamPost](../../models/components/bodystreamchapteraudiov1studioprojectsprojectidchapterschapteridsnapshotschaptersnapshotidstreampost.md) | :heavy_minus_sign:                                                                                                                                                                                                                                  | N/A                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                     |
| `opts`                                                                                                                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                            | :heavy_minus_sign:                                                                                                                                                                                                                                  | The options for this request.                                                                                                                                                                                                                       |                                                                                                                                                                                                                                                     |

### Response

**[*operations.StreamChapterSnapshotAudioResponse](../../models/operations/streamchaptersnapshotaudioresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetProjectMutedTracksEndpoint

Returns a list of chapter IDs that have muted tracks in a project.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_project_muted_tracks_endpoint" method="get" path="/v1/studio/projects/{project_id}/muted-tracks" -->
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

    res, err := s.Studio.GetProjectMutedTracksEndpoint(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.ProjectMutedTracksResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `projectID`                                              | `string`                                                 | :heavy_check_mark:                                       | The ID of the Studio project.                            | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetProjectMutedTracksEndpointResponse](../../models/operations/getprojectmutedtracksendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |