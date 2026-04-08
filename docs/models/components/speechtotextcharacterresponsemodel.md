# SpeechToTextCharacterResponseModel


## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `Text`                                       | `string`                                     | :heavy_check_mark:                           | The character that was transcribed.          |
| `Start`                                      | optionalnullable.OptionalNullable[`float64`] | :heavy_minus_sign:                           | The start time of the character in seconds.  |
| `End`                                        | optionalnullable.OptionalNullable[`float64`] | :heavy_minus_sign:                           | The end time of the character in seconds.    |