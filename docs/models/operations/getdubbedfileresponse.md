# GetDubbedFileResponse


## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `HTTPMeta`                                                         | [components.HTTPMetadata](../../models/components/httpmetadata.md) | :heavy_check_mark:                                                 | N/A                                                                |
| `TwoHundredAudioMpegResponseStream`                                | `io.ReadCloser`                                                    | :heavy_minus_sign:                                                 | The dubbed audio or video file                                     |
| `TwoHundredVideoMp4ResponseStream`                                 | `io.ReadCloser`                                                    | :heavy_minus_sign:                                                 | The dubbed audio or video file                                     |