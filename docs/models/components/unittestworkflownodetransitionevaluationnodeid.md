# UnitTestWorkflowNodeTransitionEvaluationNodeID


## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `Type`                                                           | `*string`                                                        | :heavy_minus_sign:                                               | N/A                                                              |
| `AgentID`                                                        | `string`                                                         | :heavy_check_mark:                                               | The ID of the agent whose workflow contains the target node.     |
| `TargetNodeID`                                                   | `string`                                                         | :heavy_check_mark:                                               | The ID of the workflow node that the agent should transition to. |