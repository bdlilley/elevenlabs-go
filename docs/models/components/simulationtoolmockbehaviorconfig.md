# SimulationToolMockBehaviorConfig

Simulation/preview-side config: tools are identified by IDs, resolved to names at runtime.


## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `MockingStrategy`                                                                 | [*components.MockingStrategy](../../models/components/mockingstrategy.md)         | :heavy_minus_sign:                                                                | N/A                                                                               |
| `FallbackStrategy`                                                                | [*components.MockNoMatchBehavior](../../models/components/mocknomatchbehavior.md) | :heavy_minus_sign:                                                                | N/A                                                                               |
| `MockedToolIds`                                                                   | []`string`                                                                        | :heavy_minus_sign:                                                                | Tool IDs to mock. Resolved to tool names before being passed to the orchestrator. |