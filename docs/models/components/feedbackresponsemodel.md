# FeedbackResponseModel


## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `ThumbsUp`                                                 | `bool`                                                     | :heavy_check_mark:                                         | Whether the user liked the generated item.                 |
| `Feedback`                                                 | `string`                                                   | :heavy_check_mark:                                         | The feedback text provided by the user.                    |
| `Emotions`                                                 | `bool`                                                     | :heavy_check_mark:                                         | Whether the user provided emotions.                        |
| `InaccurateClone`                                          | `bool`                                                     | :heavy_check_mark:                                         | Whether the user thinks the clone is inaccurate.           |
| `Glitches`                                                 | `bool`                                                     | :heavy_check_mark:                                         | Whether the user thinks there are glitches in the audio.   |
| `AudioQuality`                                             | `bool`                                                     | :heavy_check_mark:                                         | Whether the user thinks the audio quality is good.         |
| `Other`                                                    | `bool`                                                     | :heavy_check_mark:                                         | Whether the user provided other feedback.                  |
| `ReviewStatus`                                             | `*string`                                                  | :heavy_minus_sign:                                         | The review status of the item. Defaults to 'not_reviewed'. |