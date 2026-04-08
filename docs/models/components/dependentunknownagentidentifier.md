# DependentUnknownAgentIdentifier

A model that represents an agent dependent on a knowledge base/tools
to which the user has no direct access.


## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `ReferencedResourceIds`                                                                                   | []`string`                                                                                                | :heavy_minus_sign:                                                                                        | If the agent is a transitive dependent, contains IDs of the resources that the agent depends on directly. |
| `Type`                                                                                                    | `*string`                                                                                                 | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |