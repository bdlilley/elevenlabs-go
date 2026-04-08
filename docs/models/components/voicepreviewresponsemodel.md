# VoicePreviewResponseModel


## Fields

| Field                                                                     | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `AudioBase64`                                                             | `string`                                                                  | :heavy_check_mark:                                                        | The base64 encoded audio of the preview.                                  |
| `GeneratedVoiceID`                                                        | `string`                                                                  | :heavy_check_mark:                                                        | The ID of the generated voice. Use it to create a voice from the preview. |
| `MediaType`                                                               | `string`                                                                  | :heavy_check_mark:                                                        | The media type of the preview.                                            |
| `DurationSecs`                                                            | `float64`                                                                 | :heavy_check_mark:                                                        | The duration of the preview in seconds.                                   |
| `Language`                                                                | `*string`                                                                 | :heavy_check_mark:                                                        | The language of the preview.                                              |