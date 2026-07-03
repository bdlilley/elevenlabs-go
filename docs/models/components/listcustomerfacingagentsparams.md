# ListCustomerFacingAgentsParams

List every customer-facing agent on the workspace.

The assistant uses this whenever it needs to act on a specific customer-facing
agent (rules, config edits, etc.) so it can pick the right ``agent_id`` to pass
to mutating tools. Mirrors the ``list_services`` / ``list_clients``
pattern: read once, then mutate by id.


## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `SmbToolType`      | `*string`          | :heavy_minus_sign: | N/A                |