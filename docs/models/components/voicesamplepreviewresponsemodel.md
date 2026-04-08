# VoiceSamplePreviewResponseModel


## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `AudioBase64`                         | `string`                              | :heavy_check_mark:                    | The base64 encoded audio.             |
| `VoiceID`                             | `string`                              | :heavy_check_mark:                    | The ID of the voice.                  |
| `SampleID`                            | `string`                              | :heavy_check_mark:                    | The ID of the sample.                 |
| `MediaType`                           | `string`                              | :heavy_check_mark:                    | The media type of the audio.          |
| `DurationSecs`                        | `*float64`                            | :heavy_minus_sign:                    | The duration of the audio in seconds. |