# VoiceSegment


## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `VoiceID`                                                     | `string`                                                      | :heavy_check_mark:                                            | The voice ID used for this segment                            |
| `StartTimeSeconds`                                            | `float64`                                                     | :heavy_check_mark:                                            | Start time of this voice segment                              |
| `EndTimeSeconds`                                              | `float64`                                                     | :heavy_check_mark:                                            | End time of this voice segment                                |
| `CharacterStartIndex`                                         | `int64`                                                       | :heavy_check_mark:                                            | Start index in the characters array                           |
| `CharacterEndIndex`                                           | `int64`                                                       | :heavy_check_mark:                                            | End index in the characters array (exclusive)                 |
| `DialogueInputIndex`                                          | `int64`                                                       | :heavy_check_mark:                                            | Line of the dialogue (script) that this segment is a part of. |