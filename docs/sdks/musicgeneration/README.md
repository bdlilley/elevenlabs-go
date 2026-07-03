# MusicGeneration

## Overview

Generate music from a text prompt.

### Available Operations

* [ComposePlan](#composeplan) - Generate Composition Plan
* [Generate](#generate) - Compose Music
* [ComposeDetailed](#composedetailed) - Compose Music With A Detailed Response
* [ComposeDetailedStream](#composedetailedstream) - Stream Composed Music With A Detailed Response
* [StreamCompose](#streamcompose) - Stream Composed Music
* [UploadSong](#uploadsong) - Upload Music
* [SeparateSongStems](#separatesongstems) - Stem Separation

## ComposePlan

Generate a composition plan from a prompt.

### Example Usage

<!-- UsageSnippet language="go" operationID="compose_plan" method="post" path="/v1/music/plan" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.MusicGeneration.ComposePlan(ctx, components.BodyGenerateCompositionPlanV1MusicPlanPost{
        Prompt: "<value>",
        SourceCompositionPlan: elevenlabsgo.Pointer(components.CreateSourceCompositionPlanMusicPrompt(
            components.MusicPrompt{
                PositiveGlobalStyles: []string{
                    "pop",
                    "rock",
                    "jazz",
                },
                NegativeGlobalStyles: []string{
                    "metal",
                    "hip-hop",
                    "country",
                },
                Sections: []components.SongSection{
                    components.SongSection{
                        SectionName: "Verse 1",
                        PositiveLocalStyles: []string{
                            "pop",
                            "rock",
                            "jazz",
                        },
                        NegativeLocalStyles: []string{
                            "metal",
                            "hip-hop",
                            "country",
                        },
                        DurationMs: 10000,
                        Lines: []string{
                            "Verse 1 lyrics",
                        },
                    },
                },
            },
        )),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGenerateCompositionPlanV1MusicPlanPost != nil {
        switch res.ResponseGenerateCompositionPlanV1MusicPlanPost.Type {
            case operations.ResponseGenerateCompositionPlanV1MusicPlanPostTypeMusicPrompt:
                // res.ResponseGenerateCompositionPlanV1MusicPlanPost.MusicPrompt is populated
            case operations.ResponseGenerateCompositionPlanV1MusicPlanPostTypeCompositionPlan:
                // res.ResponseGenerateCompositionPlanV1MusicPlanPost.CompositionPlan is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                                      | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                          | :heavy_check_mark:                                                                                                             | The context to use for the request.                                                                                            |
| `request`                                                                                                                      | [components.BodyGenerateCompositionPlanV1MusicPlanPost](../../models/components/bodygeneratecompositionplanv1musicplanpost.md) | :heavy_check_mark:                                                                                                             | The request object to use for the request.                                                                                     |
| `opts`                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                       | :heavy_minus_sign:                                                                                                             | The options for this request.                                                                                                  |

### Response

**[*operations.ComposePlanResponse](../../models/operations/composeplanresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## Generate

Compose a song from a prompt or a composition plan.

### Example Usage

<!-- UsageSnippet language="go" operationID="generate" method="post" path="/v1/music" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.MusicGeneration.Generate(ctx, operations.GenerateOutputFormatOfTheGeneratedAudioAuto.ToPointer(), &components.BodyComposeMusicV1MusicPost{
        CompositionPlan: elevenlabsgo.Pointer(components.CreateBodyComposeMusicV1MusicPostCompositionPlanMusicPrompt(
            components.MusicPrompt{
                PositiveGlobalStyles: []string{
                    "pop",
                    "rock",
                    "jazz",
                },
                NegativeGlobalStyles: []string{
                    "metal",
                    "hip-hop",
                    "country",
                },
                Sections: []components.SongSection{
                    components.SongSection{
                        SectionName: "Verse 1",
                        PositiveLocalStyles: []string{
                            "pop",
                            "rock",
                            "jazz",
                        },
                        NegativeLocalStyles: []string{
                            "metal",
                            "hip-hop",
                            "country",
                        },
                        DurationMs: 10000,
                        Lines: []string{
                            "Verse 1 lyrics",
                        },
                    },
                },
            },
        )),
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

| Parameter                                                                                                                                                                                                                        | Type                                                                                                                                                                                                                             | Required                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                               | The context to use for the request.                                                                                                                                                                                              |
| `outputFormat`                                                                                                                                                                                                                   | [*operations.GenerateOutputFormatOfTheGeneratedAudio](../../models/operations/generateoutputformatofthegeneratedaudio.md)                                                                                                        | :heavy_minus_sign:                                                                                                                                                                                                               | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models.  |
| `body`                                                                                                                                                                                                                           | [*components.BodyComposeMusicV1MusicPost](../../models/components/bodycomposemusicv1musicpost.md)                                                                                                                                | :heavy_minus_sign:                                                                                                                                                                                                               | N/A                                                                                                                                                                                                                              |
| `opts`                                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                                    |

### Response

**[*operations.GenerateResponse](../../models/operations/generateresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ComposeDetailed

Compose a song from a prompt or a composition plan.

### Example Usage

<!-- UsageSnippet language="go" operationID="compose_detailed" method="post" path="/v1/music/detailed" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.MusicGeneration.ComposeDetailed(ctx, operations.ComposeDetailedOutputFormatOfTheGeneratedAudioAuto.ToPointer(), &components.BodyComposeMusicWithADetailedResponseV1MusicDetailedPost{
        CompositionPlan: elevenlabsgo.Pointer(components.CreateBodyComposeMusicWithADetailedResponseV1MusicDetailedPostCompositionPlanMusicPrompt(
            components.MusicPrompt{
                PositiveGlobalStyles: []string{
                    "pop",
                    "rock",
                    "jazz",
                },
                NegativeGlobalStyles: []string{
                    "metal",
                    "hip-hop",
                    "country",
                },
                Sections: []components.SongSection{
                    components.SongSection{
                        SectionName: "Verse 1",
                        PositiveLocalStyles: []string{
                            "pop",
                            "rock",
                            "jazz",
                        },
                        NegativeLocalStyles: []string{
                            "metal",
                            "hip-hop",
                            "country",
                        },
                        DurationMs: 10000,
                        Lines: []string{
                            "Verse 1 lyrics",
                        },
                    },
                },
            },
        )),
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

| Parameter                                                                                                                                                                                                                        | Type                                                                                                                                                                                                                             | Required                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                               | The context to use for the request.                                                                                                                                                                                              |
| `outputFormat`                                                                                                                                                                                                                   | [*operations.ComposeDetailedOutputFormatOfTheGeneratedAudio](../../models/operations/composedetailedoutputformatofthegeneratedaudio.md)                                                                                          | :heavy_minus_sign:                                                                                                                                                                                                               | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models.  |
| `body`                                                                                                                                                                                                                           | [*components.BodyComposeMusicWithADetailedResponseV1MusicDetailedPost](../../models/components/bodycomposemusicwithadetailedresponsev1musicdetailedpost.md)                                                                      | :heavy_minus_sign:                                                                                                                                                                                                               | N/A                                                                                                                                                                                                                              |
| `opts`                                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                                    |

### Response

**[*operations.ComposeDetailedResponse](../../models/operations/composedetailedresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ComposeDetailedStream

Stream a song and its detailed metadata using Server-Sent Events (SSE).

### Example Usage

<!-- UsageSnippet language="go" operationID="compose_detailed_stream" method="post" path="/v1/music/detailed/stream" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.MusicGeneration.ComposeDetailedStream(ctx, operations.ComposeDetailedStreamOutputFormatOfTheGeneratedAudioAuto.ToPointer(), &components.BodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPost{
        CompositionPlan: elevenlabsgo.Pointer(components.CreateBodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPostCompositionPlanMusicPrompt(
            components.MusicPrompt{
                PositiveGlobalStyles: []string{
                    "pop",
                    "rock",
                    "jazz",
                },
                NegativeGlobalStyles: []string{
                    "metal",
                    "hip-hop",
                    "country",
                },
                Sections: []components.SongSection{
                    components.SongSection{
                        SectionName: "Verse 1",
                        PositiveLocalStyles: []string{
                            "pop",
                            "rock",
                            "jazz",
                        },
                        NegativeLocalStyles: []string{
                            "metal",
                            "hip-hop",
                            "country",
                        },
                        DurationMs: 10000,
                        Lines: []string{
                            "Verse 1 lyrics",
                        },
                    },
                },
            },
        )),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                        | Type                                                                                                                                                                                                                             | Required                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                               | The context to use for the request.                                                                                                                                                                                              |
| `outputFormat`                                                                                                                                                                                                                   | [*operations.ComposeDetailedStreamOutputFormatOfTheGeneratedAudio](../../models/operations/composedetailedstreamoutputformatofthegeneratedaudio.md)                                                                              | :heavy_minus_sign:                                                                                                                                                                                                               | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models.  |
| `body`                                                                                                                                                                                                                           | [*components.BodyStreamComposedMusicWithADetailedResponseV1MusicDetailedStreamPost](../../models/components/bodystreamcomposedmusicwithadetailedresponsev1musicdetailedstreampost.md)                                            | :heavy_minus_sign:                                                                                                                                                                                                               | N/A                                                                                                                                                                                                                              |
| `opts`                                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                                    |

### Response

**[*operations.ComposeDetailedStreamResponse](../../models/operations/composedetailedstreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## StreamCompose

Stream a composed song from a prompt or a composition plan.

### Example Usage

<!-- UsageSnippet language="go" operationID="stream_compose" method="post" path="/v1/music/stream" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.MusicGeneration.StreamCompose(ctx, operations.StreamComposeOutputFormatOfTheGeneratedAudioAuto.ToPointer(), &components.BodyStreamComposedMusicV1MusicStreamPost{
        CompositionPlan: elevenlabsgo.Pointer(components.CreateBodyStreamComposedMusicV1MusicStreamPostCompositionPlanMusicPrompt(
            components.MusicPrompt{
                PositiveGlobalStyles: []string{
                    "pop",
                    "rock",
                    "jazz",
                },
                NegativeGlobalStyles: []string{
                    "metal",
                    "hip-hop",
                    "country",
                },
                Sections: []components.SongSection{
                    components.SongSection{
                        SectionName: "Verse 1",
                        PositiveLocalStyles: []string{
                            "pop",
                            "rock",
                            "jazz",
                        },
                        NegativeLocalStyles: []string{
                            "metal",
                            "hip-hop",
                            "country",
                        },
                        DurationMs: 10000,
                        Lines: []string{
                            "Verse 1 lyrics",
                        },
                    },
                },
            },
        )),
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

| Parameter                                                                                                                                                                                                                        | Type                                                                                                                                                                                                                             | Required                                                                                                                                                                                                                         | Description                                                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                               | The context to use for the request.                                                                                                                                                                                              |
| `outputFormat`                                                                                                                                                                                                                   | [*operations.StreamComposeOutputFormatOfTheGeneratedAudio](../../models/operations/streamcomposeoutputformatofthegeneratedaudio.md)                                                                                              | :heavy_minus_sign:                                                                                                                                                                                                               | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. Use "auto" (the default) to let the API pick the best format for the selected model: mp3_44100_128 for v1 models and mp3_48000_192 for v2 models.  |
| `body`                                                                                                                                                                                                                           | [*components.BodyStreamComposedMusicV1MusicStreamPost](../../models/components/bodystreamcomposedmusicv1musicstreampost.md)                                                                                                      | :heavy_minus_sign:                                                                                                                                                                                                               | N/A                                                                                                                                                                                                                              |
| `opts`                                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                                    |

### Response

**[*operations.StreamComposeResponse](../../models/operations/streamcomposeresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UploadSong

Upload a music file to be later used for inpainting. Price for uploading is the same as the one for song generation. All uploaded content gets inspected for copyright infringement. If copyrighted content is detected, half of the request cost is still charged.

### Example Usage

<!-- UsageSnippet language="go" operationID="upload_song" method="post" path="/v1/music/upload" -->
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

    res, err := s.MusicGeneration.UploadSong(ctx, components.BodyUploadMusicV1MusicUploadPost{
        File: components.BodyUploadMusicV1MusicUploadPostFile{
            FileName: "example.file",
            Content: example,
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MusicUploadResponse != nil {
        switch res.MusicUploadResponse.CompositionPlan.Type {
            case components.MusicUploadResponseCompositionPlanTypeMusicPrompt:
                // res.MusicUploadResponse.CompositionPlan.MusicPrompt is populated
            case components.MusicUploadResponseCompositionPlanTypeCompositionPlan:
                // res.MusicUploadResponse.CompositionPlan.CompositionPlan is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `request`                                                                                                  | [components.BodyUploadMusicV1MusicUploadPost](../../models/components/bodyuploadmusicv1musicuploadpost.md) | :heavy_check_mark:                                                                                         | The request object to use for the request.                                                                 |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

### Response

**[*operations.UploadSongResponse](../../models/operations/uploadsongresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SeparateSongStems

Separate an audio file into individual stems. This endpoint might have high latency, depending on the length of the audio file.

### Example Usage

<!-- UsageSnippet language="go" operationID="separate_song_stems" method="post" path="/v1/music/stem-separation" -->
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

    res, err := s.MusicGeneration.SeparateSongStems(ctx, components.BodyStemSeparationV1MusicStemSeparationPost{
        File: components.BodyStemSeparationV1MusicStemSeparationPostFile{
            FileName: "example.file",
            Content: example,
        },
    }, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.BodyStemSeparationV1MusicStemSeparationPost](../../models/components/bodystemseparationv1musicstemseparationpost.md)                                                                                                                                                                                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.SeparateSongStemsResponse](../../models/operations/separatesongstemsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |