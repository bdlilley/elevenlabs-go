# ASRConversationalConfigWorkflowOverride


## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `Quality`                                                               | [*components.ASRQuality](../../models/components/asrquality.md)         | :heavy_minus_sign:                                                      | The quality of the transcription                                        |
| `Provider`                                                              | [*components.ASRProvider](../../models/components/asrprovider.md)       | :heavy_minus_sign:                                                      | The provider of the transcription service                               |
| `UserInputAudioFormat`                                                  | [*components.ASRInputFormat](../../models/components/asrinputformat.md) | :heavy_minus_sign:                                                      | The format of the audio to be transcribed                               |
| `Keywords`                                                              | []`string`                                                              | :heavy_minus_sign:                                                      | Keywords to boost prediction probability for                            |