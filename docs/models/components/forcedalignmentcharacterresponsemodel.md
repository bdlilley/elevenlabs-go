# ForcedAlignmentCharacterResponseModel

Model representing a single character with its timing information from the aligner.


## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `Text`                                      | `string`                                    | :heavy_check_mark:                          | The character that was transcribed.         |
| `Start`                                     | `float64`                                   | :heavy_check_mark:                          | The start time of the character in seconds. |
| `End`                                       | `float64`                                   | :heavy_check_mark:                          | The end time of the character in seconds.   |