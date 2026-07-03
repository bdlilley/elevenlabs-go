# ApiKey

## Overview

Manage API keys for your workspace.

### Available Operations

* [Disable](#disable) - Disable Api Key
* [SetThirdPartyDisablingPolicy](#setthirdpartydisablingpolicy) - Set Workspace Third-Party Disabling Policy

## Disable

Disable the API key used to authenticate this request. Requires the query parameter `api_key_name=self` as an explicit confirmation.

### Example Usage

<!-- UsageSnippet language="go" operationID="disable" method="post" path="/v1/workspaces/api-keys/disable" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.APIKey.Disable(ctx, "<value>")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                           | Type                                                                                                                                                                | Required                                                                                                                                                            | Description                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                                               | :heavy_check_mark:                                                                                                                                                  | The context to use for the request.                                                                                                                                 |
| `apiKeyName`                                                                                                                                                        | `string`                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                  | Must be set to `self` to disable the API key used to authenticate this request. Required as an explicit confirmation to avoid accidentally disabling the wrong key. |
| `opts`                                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                                            | :heavy_minus_sign:                                                                                                                                                  | The options for this request.                                                                                                                                       |

### Response

**[*operations.DisableResponse](../../models/operations/disableresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SetThirdPartyDisablingPolicy

Set the workspace-wide Third-Party Disabling policy. When set, it forces, for every API key in the workspace, whether the holder of a key (potentially a third party who found it) may disable it via the self-disable endpoint or when it leaks publicly — overriding each key's own setting. Pass `true` to allow it for all keys, `false` to forbid it for all keys, or `null` to clear the override so per-key values and the plan default apply again. Workspace admins only.

### Example Usage

<!-- UsageSnippet language="go" operationID="set_third_party_disabling_policy" method="post" path="/v1/workspaces/api-keys/third-party-disabling" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.APIKey.SetThirdPartyDisablingPolicy(ctx, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                        | Type                                                                                                                                                                                                             | Required                                                                                                                                                                                                         | Description                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                               | The context to use for the request.                                                                                                                                                                              |
| `request`                                                                                                                                                                                                        | [components.BodySetWorkspaceThirdPartyDisablingPolicyV1WorkspacesAPIKeysThirdPartyDisablingPost](../../models/components/bodysetworkspacethirdpartydisablingpolicyv1workspacesapikeysthirdpartydisablingpost.md) | :heavy_check_mark:                                                                                                                                                                                               | The request object to use for the request.                                                                                                                                                                       |
| `opts`                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                    |

### Response

**[*operations.SetThirdPartyDisablingPolicyResponse](../../models/operations/setthirdpartydisablingpolicyresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |