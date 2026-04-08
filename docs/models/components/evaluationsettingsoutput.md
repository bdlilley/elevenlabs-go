# EvaluationSettingsOutput

Settings to evaluate an agent's performance.
Agents are evaluated against a set of criteria, with success being defined as meeting some combination of those criteria.


## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `Criteria`                                                                                   | [][components.PromptEvaluationCriteria](../../models/components/promptevaluationcriteria.md) | :heavy_minus_sign:                                                                           | Individual criteria that the agent should be evaluated against                               |