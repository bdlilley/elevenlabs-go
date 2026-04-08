# MCPToolApprovalHash

Model for storing tool approval hashes for per-tool approval.


## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `ToolName`                                                                            | `string`                                                                              | :heavy_check_mark:                                                                    | The name of the MCP tool                                                              |
| `ToolHash`                                                                            | `string`                                                                              | :heavy_check_mark:                                                                    | SHA256 hash of the tool's parameters and description                                  |
| `ApprovalPolicy`                                                                      | [*components.MCPToolApprovalPolicy](../../models/components/mcptoolapprovalpolicy.md) | :heavy_minus_sign:                                                                    | Defines the tool-level approval policy.                                               |