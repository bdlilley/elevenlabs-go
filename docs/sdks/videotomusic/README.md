# VideoToMusic

## Overview

### Available Operations

* [VideoToMusic](#videotomusic) - Video To Music

## VideoToMusic

Generate background music from one or more video files. Videos are combined in order. Optional description and style tags influence the generated music.

### Example Usage

<!-- UsageSnippet language="go" operationID="video_to_music" method="post" path="/v1/music/video-to-music" -->
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

    res, err := s.VideoToMusic.VideoToMusic(ctx, components.BodyVideoToMusicV1MusicVideoToMusicPost{
        Videos: []components.Video{
            components.Video{
                FileName: "example.file",
                Content: example,
            },
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
| `body`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [components.BodyVideoToMusicV1MusicVideoToMusicPost](../../models/components/bodyvideotomusicv1musicvideotomusicpost.md)                                                                                                                                                                                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                                                                                                                                                                                                                                                                        | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `outputFormat`                                                                                                                                                                                                                                                                                                                                                                                                                                            | [*components.AllowedOutputFormats](../../models/components/allowedoutputformats.md)                                                                                                                                                                                                                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | Output format of the generated audio. Formatted as codec_sample_rate_bitrate. So an mp3 with 22.05kHz sample rate at 32kbs is represented as mp3_22050_32. MP3 with 192kbps bitrate requires you to be subscribed to Creator tier or above. PCM with 44.1kHz sample rate requires you to be subscribed to Pro tier or above. Note that the μ-law format (sometimes written mu-law, often approximated as u-law) is commonly used for Twilio audio inputs. |
| `opts`                                                                                                                                                                                                                                                                                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                                                                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                                                                                                                                                                                                                                                                                        | The options for this request.                                                                                                                                                                                                                                                                                                                                                                                                                             |

### Response

**[*operations.VideoToMusicResponse](../../models/operations/videotomusicresponse.md), error**

### Errors

| Error Type         | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| apierrors.APIError | 4XX, 5XX           | \*/\*              |