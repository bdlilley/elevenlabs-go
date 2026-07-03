# OrderMediaResponse


## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `MediaID`                                                     | `string`                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `Name`                                                        | `string`                                                      | :heavy_check_mark:                                            | The original filename of the uploaded media.                  |
| `ContentType`                                                 | `string`                                                      | :heavy_check_mark:                                            | The MIME type of the media file (e.g. 'video/mp4').           |
| `Language`                                                    | `*string`                                                     | :heavy_minus_sign:                                            | The detected or declared language of the media, if available. |
| `SignedURL`                                                   | `string`                                                      | :heavy_check_mark:                                            | A time-limited URL to download the media file.                |