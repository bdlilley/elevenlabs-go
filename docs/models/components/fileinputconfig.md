# FileInputConfig


## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `Enabled`                                                                                     | `*bool`                                                                                       | :heavy_minus_sign:                                                                            | When enabled, users may attach images or PDFs in chat when the LLM supports multimodal input. |
| `MaxFilesPerConversation`                                                                     | `*int64`                                                                                      | :heavy_minus_sign:                                                                            | Maximum number of files that can be uploaded per conversation.                                |