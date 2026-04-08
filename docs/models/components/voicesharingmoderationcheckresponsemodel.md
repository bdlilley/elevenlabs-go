# VoiceSharingModerationCheckResponseModel


## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `DateCheckedUnix`                                    | `*int64`                                             | :heavy_minus_sign:                                   | The date the moderation check was made in Unix time. |
| `NameValue`                                          | `*string`                                            | :heavy_minus_sign:                                   | The name value of the voice.                         |
| `NameCheck`                                          | `*bool`                                              | :heavy_minus_sign:                                   | Whether the name check was successful.               |
| `DescriptionValue`                                   | `*string`                                            | :heavy_minus_sign:                                   | The description value of the voice.                  |
| `DescriptionCheck`                                   | `*bool`                                              | :heavy_minus_sign:                                   | Whether the description check was successful.        |
| `SampleIds`                                          | []`string`                                           | :heavy_minus_sign:                                   | A list of sample IDs.                                |
| `SampleChecks`                                       | []`float64`                                          | :heavy_minus_sign:                                   | A list of sample checks.                             |
| `CaptchaIds`                                         | []`string`                                           | :heavy_minus_sign:                                   | A list of captcha IDs.                               |
| `CaptchaChecks`                                      | []`float64`                                          | :heavy_minus_sign:                                   | A list of CAPTCHA check values.                      |