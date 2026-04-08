# ForcedAlignment

## Overview

Force align an audio file to a text transcript to get precise word-level and character level timing information. Response is a list of characters with their start and end times as milliseconds elapsed from the start of the recording.

### Available Operations

* [ForcedAlignment](#forcedalignment) - Create Forced Alignment

## ForcedAlignment

Force align an audio file to text. Use this endpoint to get the timing information for each character and word in an audio file based on a provided text transcript.

### Example Usage

<!-- UsageSnippet language="go" operationID="forced_alignment" method="post" path="/v1/forced-alignment" -->
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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.ForcedAlignment.ForcedAlignment(ctx, components.BodyCreateForcedAlignmentV1ForcedAlignmentPost{
        File: components.BodyCreateForcedAlignmentV1ForcedAlignmentPostFile{
            FileName: "example.file",
            Content: example,
        },
        Text: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ForcedAlignmentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyCreateForcedAlignmentV1ForcedAlignmentPost](../../models/components/bodycreateforcedalignmentv1forcedalignmentpost.md)                    | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.ForcedAlignmentResponse](../../models/operations/forcedalignmentresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |