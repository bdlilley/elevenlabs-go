# OrchestratorToolMockBehaviorConfig

Orchestrator-side config: tools are identified by resolved names.


## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `MockingStrategy`                                                                 | [*components.MockingStrategy](../../models/components/mockingstrategy.md)         | :heavy_minus_sign:                                                                | N/A                                                                               |
| `FallbackStrategy`                                                                | [*components.MockNoMatchBehavior](../../models/components/mocknomatchbehavior.md) | :heavy_minus_sign:                                                                | N/A                                                                               |
| `MockedToolNames`                                                                 | []`string`                                                                        | :heavy_minus_sign:                                                                | Tool names to mock. Only used when mocking_strategy is 'selected'.                |