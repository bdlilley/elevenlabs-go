# GetOrCreateRAGIndexRequestModel


## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `DocumentID`                                                                    | `string`                                                                        | :heavy_check_mark:                                                              | ID of the knowledgebase document for which to retrieve the index                |
| `CreateIfMissing`                                                               | `bool`                                                                          | :heavy_check_mark:                                                              | Whether to create the RAG index if it does not exist                            |
| `Model`                                                                         | [*components.EmbeddingModelEnum](../../models/components/embeddingmodelenum.md) | :heavy_minus_sign:                                                              | N/A                                                                             |