# ResponseFilter

Configuration for filtering tool responses before they are visible to the agent.


## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `Mode`                                                                                     | [*components.ResponseFilterMode](../../models/components/responsefiltermode.md)            | :heavy_minus_sign:                                                                         | Controls how tool responses are filtered before being visible to the agent.                |
| `Filters`                                                                                  | []`string`                                                                                 | :heavy_minus_sign:                                                                         | Dot notation paths to include when mode is 'allow' (e.g., ['ticket.id', 'ticket.status']). |
| `ContentType`                                                                              | `*string`                                                                                  | :heavy_minus_sign:                                                                         | Content type for response filtering. Only 'application/json' responses are filtered.       |