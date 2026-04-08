# MusicGeneration

## Overview

### Available Operations

* [ComposePlan](#composeplan) - Generate Composition Plan
* [Generate](#generate) - Compose Music
* [ComposeDetailed](#composedetailed) - Compose Music With A Detailed Response
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
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.MusicGeneration.ComposePlan(ctx, components.BodyGenerateCompositionPlanV1MusicPlanPost{
        Prompt: "<value>",
        SourceCompositionPlan: optionalnullable.From(&components.MusicPrompt{
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
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MusicPrompt != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyGenerateCompositionPlanV1MusicPlanPost](../../models/components/bodygeneratecompositionplanv1musicplanpost.md)                            | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

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
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.MusicGeneration.Generate(ctx, nil, optionalnullable.From[string](nil), &components.BodyComposeMusicV1MusicPost{
        CompositionPlan: optionalnullable.From(&components.MusicPrompt{
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
        }),
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

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [*components.BodyComposeMusicV1MusicPost](../../models/components/bodycomposemusicv1musicpost.md)                                                                                                                                                                                                                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

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
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.MusicGeneration.ComposeDetailed(ctx, nil, optionalnullable.From[string](nil), &components.BodyComposeMusicWithADetailedResponseV1MusicDetailedPost{
        CompositionPlan: optionalnullable.From(&components.MusicPrompt{
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
        }),
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

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [*components.BodyComposeMusicWithADetailedResponseV1MusicDetailedPost](../../models/components/bodycomposemusicwithadetailedresponsev1musicdetailedpost.md)                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.ComposeDetailedResponse](../../models/operations/composedetailedresponse.md), error**

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
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.MusicGeneration.StreamCompose(ctx, nil, optionalnullable.From[string](nil), &components.BodyStreamComposedMusicV1MusicStreamPost{
        CompositionPlan: optionalnullable.From(&components.MusicPrompt{
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
        }),
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

| Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Required                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The context to use for the request.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [*components.BodyStreamComposedMusicV1MusicStreamPost](../../models/components/bodystreamcomposedmusicv1musicstreampost.md)                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.StreamComposeResponse](../../models/operations/streamcomposeresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UploadSong

Upload a music file to be later used for inpainting. Only available to enterprise clients with access to the inpainting feature.

### Example Usage

<!-- UsageSnippet language="go" operationID="upload_song" method="post" path="/v1/music/upload" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
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
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MusicUploadResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyUploadMusicV1MusicUploadPost](../../models/components/bodyuploadmusicv1musicuploadpost.md)                                                | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

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
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
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
    }, nil, optionalnullable.From[string](nil))
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
| `xiAPIKey`                                                                                                                                                                                                                                                                                                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.SeparateSongStemsResponse](../../models/operations/separatesongstemsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |