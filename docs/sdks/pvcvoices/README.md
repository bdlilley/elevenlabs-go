# PvcVoices

## Overview

### Available Operations

* [CreatePvcVoice](#createpvcvoice) - Create Pvc Voice
* [EditPvcVoice](#editpvcvoice) - Edit Pvc Voice
* [AddPvcVoiceSamples](#addpvcvoicesamples) - Add Samples To Pvc Voice
* [EditPvcVoiceSample](#editpvcvoicesample) - Update Pvc Voice Sample
* [DeletePvcVoiceSample](#deletepvcvoicesample) - Delete Pvc Voice Sample
* [GetPvcSampleAudio](#getpvcsampleaudio) - Retrieve Voice Sample Audio
* [GetPvcSampleVisualWaveform](#getpvcsamplevisualwaveform) - Retrieve Voice Sample Visual Waveform
* [GetPvcSampleSpeakers](#getpvcsamplespeakers) - Retrieve Speaker Separation Status
* [StartSpeakerSeparation](#startspeakerseparation) - Start Speaker Separation
* [GetSpeakerAudio](#getspeakeraudio) - Retrieve Separated Speaker Audio
* [GetPvcVoiceCaptcha](#getpvcvoicecaptcha) - Get Pvc Voice Captcha
* [VerifyPvcVoiceCaptcha](#verifypvcvoicecaptcha) - Verify Pvc Voice Captcha
* [RunPvcVoiceTraining](#runpvcvoicetraining) - Run Pvc Training
* [RequestPvcManualVerification](#requestpvcmanualverification) - Request Manual Verification

## CreatePvcVoice

Creates a new PVC voice with metadata but no samples

### Example Usage

<!-- UsageSnippet language="go" operationID="create_pvc_voice" method="post" path="/v1/voices/pvc" -->
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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.PvcVoices.CreatePvcVoice(ctx, components.BodyCreatePVCVoiceV1VoicesPVCPost{
        Name: "John Smith",
        Language: "en",
        Description: optionalnullable.From(elevenlabsgo.Pointer("An old American male voice with a slight hoarseness in his throat. Perfect for news.")),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AddVoiceResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyCreatePVCVoiceV1VoicesPVCPost](../../models/components/bodycreatepvcvoicev1voicespvcpost.md)                                              | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreatePvcVoiceResponse](../../models/operations/createpvcvoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditPvcVoice

Edit PVC voice metadata

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_pvc_voice" method="post" path="/v1/voices/pvc/{voice_id}" -->
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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.PvcVoices.EditPvcVoice(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil), &components.BodyEditPVCVoiceV1VoicesPVCVoiceIDPost{
        Name: elevenlabsgo.Pointer("John Smith"),
        Language: elevenlabsgo.Pointer("en"),
        Description: optionalnullable.From(elevenlabsgo.Pointer("An old American male voice with a slight hoarseness in his throat. Perfect for news.")),
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

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `body`                                                                                                                                                    | [*components.BodyEditPVCVoiceV1VoicesPVCVoiceIDPost](../../models/components/bodyeditpvcvoicev1voicespvcvoiceidpost.md)                                   | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.EditPvcVoiceResponse](../../models/operations/editpvcvoiceresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddPvcVoiceSamples

Add audio samples to a PVC voice

### Example Usage

<!-- UsageSnippet language="go" operationID="add_pvc_voice_samples" method="post" path="/v1/voices/pvc/{voice_id}/samples" -->
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

    res, err := s.PvcVoices.AddPvcVoiceSamples(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyAddSamplesToPVCVoiceV1VoicesPVCVoiceIDSamplesPost{
        Files: []components.BodyAddSamplesToPVCVoiceV1VoicesPVCVoiceIDSamplesPostFile{},
        RemoveBackgroundNoise: elevenlabsgo.Pointer(true),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseAddSamplesToPvcVoiceV1VoicesPvcVoiceIDSamplesPost != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `body`                                                                                                                                                    | [components.BodyAddSamplesToPVCVoiceV1VoicesPVCVoiceIDSamplesPost](../../models/components/bodyaddsamplestopvcvoicev1voicespvcvoiceidsamplespost.md)      | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.AddPvcVoiceSamplesResponse](../../models/operations/addpvcvoicesamplesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditPvcVoiceSample

Update a PVC voice sample - apply noise removal, select speaker, change trim times or file name.

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_pvc_voice_sample" method="post" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}" -->
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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.PvcVoices.EditPvcVoiceSample(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil), &components.BodyUpdatePVCVoiceSampleV1VoicesPVCVoiceIDSamplesSampleIDPost{
        RemoveBackgroundNoise: elevenlabsgo.Pointer(true),
        TrimStartTime: optionalnullable.From(elevenlabsgo.Pointer[int64](0)),
        TrimEndTime: optionalnullable.From(elevenlabsgo.Pointer[int64](10)),
        FileName: optionalnullable.From(elevenlabsgo.Pointer("sample.mp3")),
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

| Parameter                                                                                                                                                             | Type                                                                                                                                                                  | Required                                                                                                                                                              | Description                                                                                                                                                           | Example                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                 | :heavy_check_mark:                                                                                                                                                    | The context to use for the request.                                                                                                                                   |                                                                                                                                                                       |
| `voiceID`                                                                                                                                                             | `string`                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                                | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                  |
| `sampleID`                                                                                                                                                            | `string`                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | Sample ID to be used                                                                                                                                                  | VW7YKqPnjY4h39yTbx2L                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                            | optionalnullable.OptionalNullable[`string`]                                                                                                                           | :heavy_minus_sign:                                                                                                                                                    | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.             |                                                                                                                                                                       |
| `body`                                                                                                                                                                | [*components.BodyUpdatePVCVoiceSampleV1VoicesPVCVoiceIDSamplesSampleIDPost](../../models/components/bodyupdatepvcvoicesamplev1voicespvcvoiceidsamplessampleidpost.md) | :heavy_minus_sign:                                                                                                                                                    | N/A                                                                                                                                                                   |                                                                                                                                                                       |
| `opts`                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                              | :heavy_minus_sign:                                                                                                                                                    | The options for this request.                                                                                                                                         |                                                                                                                                                                       |

### Response

**[*operations.EditPvcVoiceSampleResponse](../../models/operations/editpvcvoicesampleresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeletePvcVoiceSample

Delete a sample from a PVC voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_pvc_voice_sample" method="delete" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}" -->
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

    res, err := s.PvcVoices.DeletePvcVoiceSample(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteVoiceSampleResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `sampleID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Sample ID to be used                                                                                                                                      | VW7YKqPnjY4h39yTbx2L                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeletePvcVoiceSampleResponse](../../models/operations/deletepvcvoicesampleresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPvcSampleAudio

Retrieve the first 30 seconds of voice sample audio with or without noise removal.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pvc_sample_audio" method="get" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}/audio" -->
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

    res, err := s.PvcVoices.GetPvcSampleAudio(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", elevenlabsgo.Pointer(true), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoiceSamplePreviewResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                             | Type                                                                                                                                                                  | Required                                                                                                                                                              | Description                                                                                                                                                           | Example                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                 | :heavy_check_mark:                                                                                                                                                    | The context to use for the request.                                                                                                                                   |                                                                                                                                                                       |
| `voiceID`                                                                                                                                                             | `string`                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                                | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                  |
| `sampleID`                                                                                                                                                            | `string`                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | Sample ID to be used                                                                                                                                                  | VW7YKqPnjY4h39yTbx2L                                                                                                                                                  |
| `removeBackgroundNoise`                                                                                                                                               | `*bool`                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                    | If set will remove background noise for voice samples using our audio isolation model. If the samples do not include background noise, it can make the quality worse. | true                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                            | optionalnullable.OptionalNullable[`string`]                                                                                                                           | :heavy_minus_sign:                                                                                                                                                    | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.             |                                                                                                                                                                       |
| `opts`                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                              | :heavy_minus_sign:                                                                                                                                                    | The options for this request.                                                                                                                                         |                                                                                                                                                                       |

### Response

**[*operations.GetPvcSampleAudioResponse](../../models/operations/getpvcsampleaudioresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPvcSampleVisualWaveform

Retrieve the visual waveform of a voice sample.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pvc_sample_visual_waveform" method="get" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}/waveform" -->
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

    res, err := s.PvcVoices.GetPvcSampleVisualWaveform(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VoiceSampleVisualWaveformResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `sampleID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Sample ID to be used                                                                                                                                      | VW7YKqPnjY4h39yTbx2L                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetPvcSampleVisualWaveformResponse](../../models/operations/getpvcsamplevisualwaveformresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPvcSampleSpeakers

Retrieve the status of the speaker separation process and the list of detected speakers if complete.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pvc_sample_speakers" method="get" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}/speakers" -->
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

    res, err := s.PvcVoices.GetPvcSampleSpeakers(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeakerSeparationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `sampleID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Sample ID to be used                                                                                                                                      | VW7YKqPnjY4h39yTbx2L                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetPvcSampleSpeakersResponse](../../models/operations/getpvcsamplespeakersresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## StartSpeakerSeparation

Start speaker separation process for a sample

### Example Usage

<!-- UsageSnippet language="go" operationID="start_speaker_separation" method="post" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}/separate-speakers" -->
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

    res, err := s.PvcVoices.StartSpeakerSeparation(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.StartSpeakerSeparationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `sampleID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Sample ID to be used                                                                                                                                      | VW7YKqPnjY4h39yTbx2L                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.StartSpeakerSeparationResponse](../../models/operations/startspeakerseparationresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSpeakerAudio

Retrieve the separated audio for a specific speaker.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_speaker_audio" method="get" path="/v1/voices/pvc/{voice_id}/samples/{sample_id}/speakers/{speaker_id}/audio" -->
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

    res, err := s.PvcVoices.GetSpeakerAudio(ctx, "21m00Tcm4TlvDq8ikWAM", "VW7YKqPnjY4h39yTbx2L", "VW7YKqPnjY4h39yTbx2L", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SpeakerAudioResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                           | Type                                                                                                                                                                | Required                                                                                                                                                            | Description                                                                                                                                                         | Example                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                                               | :heavy_check_mark:                                                                                                                                                  | The context to use for the request.                                                                                                                                 |                                                                                                                                                                     |
| `voiceID`                                                                                                                                                           | `string`                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                  | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                              | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                |
| `sampleID`                                                                                                                                                          | `string`                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                  | Sample ID to be used                                                                                                                                                | VW7YKqPnjY4h39yTbx2L                                                                                                                                                |
| `speakerID`                                                                                                                                                         | `string`                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                  | Speaker ID to be used, you can use GET https://api.elevenlabs.io/v1/voices/{voice_id}/samples/{sample_id}/speakers to list all the available speakers for a sample. | VW7YKqPnjY4h39yTbx2L                                                                                                                                                |
| `xiAPIKey`                                                                                                                                                          | optionalnullable.OptionalNullable[`string`]                                                                                                                         | :heavy_minus_sign:                                                                                                                                                  | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.           |                                                                                                                                                                     |
| `opts`                                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                                            | :heavy_minus_sign:                                                                                                                                                  | The options for this request.                                                                                                                                       |                                                                                                                                                                     |

### Response

**[*operations.GetSpeakerAudioResponse](../../models/operations/getspeakeraudioresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPvcVoiceCaptcha

Get captcha for PVC voice verification.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pvc_voice_captcha" method="get" path="/v1/voices/pvc/{voice_id}/captcha" -->
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

    res, err := s.PvcVoices.GetPvcVoiceCaptcha(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetPvcVoiceCaptchaResponse](../../models/operations/getpvcvoicecaptcharesponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## VerifyPvcVoiceCaptcha

Submit captcha verification for PVC voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="verify_pvc_voice_captcha" method="post" path="/v1/voices/pvc/{voice_id}/captcha" -->
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

    res, err := s.PvcVoices.VerifyPvcVoiceCaptcha(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyVerifyPVCVoiceCaptchaV1VoicesPVCVoiceIDCaptchaPost{
        Recording: components.Recording{
            FileName: "example.file",
            Content: example,
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.VerifyPVCVoiceCaptchaResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `body`                                                                                                                                                    | [components.BodyVerifyPVCVoiceCaptchaV1VoicesPVCVoiceIDCaptchaPost](../../models/components/bodyverifypvcvoicecaptchav1voicespvcvoiceidcaptchapost.md)    | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.VerifyPvcVoiceCaptchaResponse](../../models/operations/verifypvcvoicecaptcharesponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RunPvcVoiceTraining

Start PVC training process for a voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_pvc_voice_training" method="post" path="/v1/voices/pvc/{voice_id}/train" -->
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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.PvcVoices.RunPvcVoiceTraining(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil), &components.BodyRunPVCTrainingV1VoicesPVCVoiceIDTrainPost{
        ModelID: optionalnullable.From(elevenlabsgo.Pointer("eleven_turbo_v2")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.StartPVCVoiceTrainingResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `voiceID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `body`                                                                                                                                                    | [*components.BodyRunPVCTrainingV1VoicesPVCVoiceIDTrainPost](../../models/components/bodyrunpvctrainingv1voicespvcvoiceidtrainpost.md)                     | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.RunPvcVoiceTrainingResponse](../../models/operations/runpvcvoicetrainingresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RequestPvcManualVerification

Request manual verification for a PVC voice.

### Example Usage

<!-- UsageSnippet language="go" operationID="request_pvc_manual_verification" method="post" path="/v1/voices/pvc/{voice_id}/verification" -->
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

    res, err := s.PvcVoices.RequestPvcManualVerification(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyRequestManualVerificationV1VoicesPvcVoiceIDVerificationPost{
        Files: []components.BodyRequestManualVerificationV1VoicesPvcVoiceIDVerificationPostFile{},
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.RequestPVCManualVerificationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                | Type                                                                                                                                                                     | Required                                                                                                                                                                 | Description                                                                                                                                                              | Example                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                    | :heavy_check_mark:                                                                                                                                                       | The context to use for the request.                                                                                                                                      |                                                                                                                                                                          |
| `voiceID`                                                                                                                                                                | `string`                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                       | Voice ID to be used, you can use https://api.elevenlabs.io/v1/voices to list all the available voices.                                                                   | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                     |
| `body`                                                                                                                                                                   | [components.BodyRequestManualVerificationV1VoicesPvcVoiceIDVerificationPost](../../models/components/bodyrequestmanualverificationv1voicespvcvoiceidverificationpost.md) | :heavy_check_mark:                                                                                                                                                       | N/A                                                                                                                                                                      |                                                                                                                                                                          |
| `xiAPIKey`                                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                                              | :heavy_minus_sign:                                                                                                                                                       | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                |                                                                                                                                                                          |
| `opts`                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                 | :heavy_minus_sign:                                                                                                                                                       | The options for this request.                                                                                                                                            |                                                                                                                                                                          |

### Response

**[*operations.RequestPvcManualVerificationResponse](../../models/operations/requestpvcmanualverificationresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |