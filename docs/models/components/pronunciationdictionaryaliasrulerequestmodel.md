# PronunciationDictionaryAliasRuleRequestModel


## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `StringToReplace`                                      | `string`                                               | :heavy_check_mark:                                     | The string to replace. Must be a non-empty string.     |
| `CaseSensitive`                                        | `*bool`                                                | :heavy_minus_sign:                                     | Whether the rule should match case-sensitively.        |
| `WordBoundaries`                                       | `*bool`                                                | :heavy_minus_sign:                                     | Whether the rule should only match at word boundaries. |
| `Type`                                                 | `string`                                               | :heavy_check_mark:                                     | The type of the rule.                                  |
| `Alias`                                                | `string`                                               | :heavy_check_mark:                                     | The alias for the string to be replaced.               |