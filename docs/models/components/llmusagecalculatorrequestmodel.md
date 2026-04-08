# LLMUsageCalculatorRequestModel


## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `PromptLength`                                                       | optionalnullable.OptionalNullable[`int64`]                           | :heavy_minus_sign:                                                   | Length of the prompt in characters.                                  |
| `NumberOfPages`                                                      | optionalnullable.OptionalNullable[`int64`]                           | :heavy_minus_sign:                                                   | Pages of content in pdf documents OR urls in agent's Knowledge Base. |
| `RagEnabled`                                                         | optionalnullable.OptionalNullable[`bool`]                            | :heavy_minus_sign:                                                   | Whether RAG is enabled.                                              |