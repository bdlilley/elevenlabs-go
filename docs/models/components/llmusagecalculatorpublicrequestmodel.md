# LLMUsageCalculatorPublicRequestModel


## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `PromptLength`                                                           | `int64`                                                                  | :heavy_check_mark:                                                       | Length of the prompt in characters.                                      |
| `NumberOfPages`                                                          | `int64`                                                                  | :heavy_check_mark:                                                       | Pages of content in PDF documents or URLs in the agent's knowledge base. |
| `RagEnabled`                                                             | `bool`                                                                   | :heavy_check_mark:                                                       | Whether RAG is enabled.                                                  |