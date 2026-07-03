# DeliverableInfo


## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `SignedURL`                                             | `string`                                                | :heavy_check_mark:                                      | A time-limited URL to download the delivered file.      |
| `ContentType`                                           | `string`                                                | :heavy_check_mark:                                      | The MIME type of the delivered file (e.g. 'video/mp4'). |
| `Name`                                                  | `string`                                                | :heavy_check_mark:                                      | The name of the delivered file.                         |
| `Version`                                               | `*int64`                                                | :heavy_minus_sign:                                      | The version number of the deliverable.                  |