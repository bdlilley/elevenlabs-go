# GetBranchesRouteRequest


## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             | Example                                                 |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `AgentID`                                               | `string`                                                | :heavy_check_mark:                                      | The id of an agent. This is returned on agent creation. | agent_3701k3ttaq12ewp8b7qv5rfyszkz                      |
| `IncludeArchived`                                       | `*bool`                                                 | :heavy_minus_sign:                                      | Whether archived branches should be included            |                                                         |
| `Limit`                                                 | `*int64`                                                | :heavy_minus_sign:                                      | How many results at most should be returned             |                                                         |