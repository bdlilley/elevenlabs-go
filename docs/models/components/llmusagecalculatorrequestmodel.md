# LLMUsageCalculatorRequestModel


## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `PromptLength`                                                       | `*int64`                                                             | :heavy_minus_sign:                                                   | Length of the prompt in characters.                                  |
| `NumberOfPages`                                                      | `*int64`                                                             | :heavy_minus_sign:                                                   | Pages of content in pdf documents OR urls in agent's Knowledge Base. |
| `RagEnabled`                                                         | `*bool`                                                              | :heavy_minus_sign:                                                   | Whether RAG is enabled.                                              |