# ListMCPToolsResponseModel

Response model for testing tools available on an MCP server.


## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `Success`                                            | `bool`                                               | :heavy_check_mark:                                   | Indicates if the operation was successful.           |
| `Tools`                                              | [][components.Tool](../../models/components/tool.md) | :heavy_check_mark:                                   | A list of tools available on the MCP server.         |
| `ErrorMessage`                                       | `*string`                                            | :heavy_minus_sign:                                   | Error message if the operation was not successful.   |