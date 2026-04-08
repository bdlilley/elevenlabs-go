# VoiceSharingModerationCheckResponseModel


## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `DateCheckedUnix`                                    | optionalnullable.OptionalNullable[`int64`]           | :heavy_minus_sign:                                   | The date the moderation check was made in Unix time. |
| `NameValue`                                          | optionalnullable.OptionalNullable[`string`]          | :heavy_minus_sign:                                   | The name value of the voice.                         |
| `NameCheck`                                          | optionalnullable.OptionalNullable[`bool`]            | :heavy_minus_sign:                                   | Whether the name check was successful.               |
| `DescriptionValue`                                   | optionalnullable.OptionalNullable[`string`]          | :heavy_minus_sign:                                   | The description value of the voice.                  |
| `DescriptionCheck`                                   | optionalnullable.OptionalNullable[`bool`]            | :heavy_minus_sign:                                   | Whether the description check was successful.        |
| `SampleIds`                                          | optionalnullable.OptionalNullable[[]`string`]        | :heavy_minus_sign:                                   | A list of sample IDs.                                |
| `SampleChecks`                                       | optionalnullable.OptionalNullable[[]`float64`]       | :heavy_minus_sign:                                   | A list of sample checks.                             |
| `CaptchaIds`                                         | optionalnullable.OptionalNullable[[]`string`]        | :heavy_minus_sign:                                   | A list of captcha IDs.                               |
| `CaptchaChecks`                                      | optionalnullable.OptionalNullable[[]`float64`]       | :heavy_minus_sign:                                   | A list of CAPTCHA check values.                      |