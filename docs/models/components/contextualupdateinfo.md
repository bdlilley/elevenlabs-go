# ContextualUpdateInfo


## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `ContextID`                                                                                    | `string`                                                                                       | :heavy_check_mark:                                                                             | Client-supplied identifier grouping related contextual updates.                                |
| `IsSuperseded`                                                                                 | `*bool`                                                                                        | :heavy_minus_sign:                                                                             | True when this contextual update has been replaced by a newer update with the same context_id. |