# VerifiedVoiceLanguageResponseModel


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `Language`                                  | `string`                                    | :heavy_check_mark:                          | The language of the voice.                  |
| `ModelID`                                   | `string`                                    | :heavy_check_mark:                          | The voice's model ID.                       |
| `Accent`                                    | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | The voice's accent, if applicable.          |
| `Locale`                                    | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | The voice's locale, if applicable.          |
| `PreviewURL`                                | optionalnullable.OptionalNullable[`string`] | :heavy_minus_sign:                          | The voice's preview URL, if applicable.     |