# RecordingResponseModel


## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `RecordingID`                           | `string`                                | :heavy_check_mark:                      | The ID of the recording.                |
| `MimeType`                              | `string`                                | :heavy_check_mark:                      | The MIME type of the recording.         |
| `SizeBytes`                             | `int64`                                 | :heavy_check_mark:                      | The size of the recording in bytes.     |
| `UploadDateUnix`                        | `int64`                                 | :heavy_check_mark:                      | The date of the recording in Unix time. |
| `Transcription`                         | `string`                                | :heavy_check_mark:                      | The transcription of the recording.     |