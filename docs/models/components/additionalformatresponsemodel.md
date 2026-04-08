# AdditionalFormatResponseModel


## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `RequestedFormat`                            | `string`                                     | :heavy_check_mark:                           | The requested format.                        |
| `FileExtension`                              | `string`                                     | :heavy_check_mark:                           | The file extension of the additional format. |
| `ContentType`                                | `string`                                     | :heavy_check_mark:                           | The content type of the additional format.   |
| `IsBase64Encoded`                            | `bool`                                       | :heavy_check_mark:                           | Whether the content is base64 encoded.       |
| `Content`                                    | `string`                                     | :heavy_check_mark:                           | The content of the additional format.        |