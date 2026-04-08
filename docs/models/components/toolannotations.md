# ToolAnnotations

Additional properties describing a Tool to clients.

NOTE: all properties in ToolAnnotations are **hints**.
They are not guaranteed to provide a faithful description of
tool behavior (including descriptive properties like `title`).

Clients should never make tool use decisions based on ToolAnnotations
received from untrusted servers.


## Fields

| Field                  | Type                   | Required               | Description            |
| ---------------------- | ---------------------- | ---------------------- | ---------------------- |
| `Title`                | `*string`              | :heavy_minus_sign:     | N/A                    |
| `ReadOnlyHint`         | `*bool`                | :heavy_minus_sign:     | N/A                    |
| `DestructiveHint`      | `*bool`                | :heavy_minus_sign:     | N/A                    |
| `IdempotentHint`       | `*bool`                | :heavy_minus_sign:     | N/A                    |
| `OpenWorldHint`        | `*bool`                | :heavy_minus_sign:     | N/A                    |
| `AdditionalProperties` | map[string]`any`       | :heavy_minus_sign:     | N/A                    |