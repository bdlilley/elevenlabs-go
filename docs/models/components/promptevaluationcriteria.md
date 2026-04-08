# PromptEvaluationCriteria

An evaluation using the transcript and a prompt for a yes/no achieved answer


## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `ID`                                                                   | `string`                                                               | :heavy_check_mark:                                                     | The unique identifier for the evaluation criteria                      |
| `Name`                                                                 | `string`                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `Type`                                                                 | `*string`                                                              | :heavy_minus_sign:                                                     | The type of evaluation criteria                                        |
| `ConversationGoalPrompt`                                               | `string`                                                               | :heavy_check_mark:                                                     | The prompt that the agent should use to evaluate the conversation      |
| `UseKnowledgeBase`                                                     | `*bool`                                                                | :heavy_minus_sign:                                                     | When evaluating the prompt, should the agent's knowledge base be used. |
| `Scope`                                                                | [*components.AnalysisScope](../../models/components/analysisscope.md)  | :heavy_minus_sign:                                                     | N/A                                                                    |