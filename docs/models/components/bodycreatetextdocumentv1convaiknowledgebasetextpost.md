# BodyCreateTextDocumentV1ConvaiKnowledgeBaseTextPost


## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `Text`                                                                         | `string`                                                                       | :heavy_check_mark:                                                             | Text content to be added to the knowledge base.                                |
| `Name`                                                                         | optionalnullable.OptionalNullable[`string`]                                    | :heavy_minus_sign:                                                             | A custom, human-readable name for the document.                                |
| `ParentFolderID`                                                               | optionalnullable.OptionalNullable[`string`]                                    | :heavy_minus_sign:                                                             | If set, the created document or folder will be placed inside the given folder. |