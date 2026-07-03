# Workspace

## Overview

Access to workspace related endpoints.

### Available Operations

* [Disable](#disable) - Disable Api Key
* [SetThirdPartyDisablingPolicy](#setthirdpartydisablingpolicy) - Set Workspace Third-Party Disabling Policy
* [GetServiceAccountAPIKeys](#getserviceaccountapikeys) - Get Service Account Api Keys Route
* [CreateServiceAccountAPIKey](#createserviceaccountapikey) - Create Service Account Api Key
* [DeleteServiceAccountAPIKey](#deleteserviceaccountapikey) - Delete Service Account Api Key
* [EditServiceAccountAPIKey](#editserviceaccountapikey) - Edit Service Account Api Key
* [GetWorkspaceAuditLogs](#getworkspaceauditlogs) - Get Workspace Audit Logs
* [ListAuthConnections](#listauthconnections) - Get Workspace Auth Connections
* [CreateAuthConnection](#createauthconnection) - Create Workspace Auth Connection
* [DeleteAuthConnection](#deleteauthconnection) - Delete Workspace Auth Connection
* [UpdateAuthConnection](#updateauthconnection) - Update Workspace Auth Connection
* [GetWorkspaceServiceAccounts](#getworkspaceserviceaccounts) - Get Workspace Service Accounts
* [GetGroupsEndpoint](#getgroupsendpoint) - Get All Groups
* [SearchGroups](#searchgroups) - Search User Groups
* [RemoveMember](#removemember) - Delete Member From User Group
* [AddMember](#addmember) - Add Member To User Group
* [InviteUser](#inviteuser) - Invite User
* [InviteUsersBulk](#inviteusersbulk) - Invite Multiple Users
* [DeleteInvite](#deleteinvite) - Delete Existing Invitation
* [UpdateWorkspaceMember](#updateworkspacemember) - Update Member
* [GetResourceMetadata](#getresourcemetadata) - Get Resource
* [ShareResourceEndpoint](#shareresourceendpoint) - Share Workspace Resource
* [UnshareResourceEndpoint](#unshareresourceendpoint) - Unshare Workspace Resource
* [GetWorkspaceWebhooks](#getworkspacewebhooks) - List Workspace Webhooks
* [CreateWorkspaceWebhook](#createworkspacewebhook) - Create Workspace Webhook
* [EditWorkspaceWebhook](#editworkspacewebhook) - Update Workspace Webhook
* [DeleteWorkspaceWebhook](#deleteworkspacewebhook) - Delete Workspace Webhook

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

    res, err := s.Workspace.Disable(ctx, "<value>")
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

    res, err := s.Workspace.SetThirdPartyDisablingPolicy(ctx, nil)
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

## GetServiceAccountAPIKeys

Get all API keys for a service account

### Example Usage

<!-- UsageSnippet language="go" operationID="get_service_account_api_keys_route" method="get" path="/v1/service-accounts/{service_account_user_id}/api-keys" -->
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

    res, err := s.Workspace.GetServiceAccountAPIKeys(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceAPIKeyListResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `serviceAccountUserID`                                   | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetServiceAccountAPIKeysRouteResponse](../../models/operations/getserviceaccountapikeysrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateServiceAccountAPIKey

Create a new API key for a service account

### Example Usage

<!-- UsageSnippet language="go" operationID="create_service_account_api_key" method="post" path="/v1/service-accounts/{service_account_user_id}/api-keys" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.CreateServiceAccountAPIKey(ctx, "<id>", components.BodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPost{
        Name: "<value>",
        Permissions: components.CreateBodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissionsArrayOfPermissionType(
            []components.PermissionType{},
        ),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceCreateAPIKeyResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                              | Type                                                                                                                                                                                                   | Required                                                                                                                                                                                               | Description                                                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                                     | The context to use for the request.                                                                                                                                                                    |
| `serviceAccountUserID`                                                                                                                                                                                 | `string`                                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                                     | N/A                                                                                                                                                                                                    |
| `body`                                                                                                                                                                                                 | [components.BodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPost](../../models/components/bodycreateserviceaccountapikeyv1serviceaccountsserviceaccountuseridapikeyspost.md) | :heavy_check_mark:                                                                                                                                                                                     | N/A                                                                                                                                                                                                    |
| `opts`                                                                                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                     | The options for this request.                                                                                                                                                                          |

### Response

**[*operations.CreateServiceAccountAPIKeyResponse](../../models/operations/createserviceaccountapikeyresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteServiceAccountAPIKey

Delete an existing API key for a service account

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_service_account_api_key" method="delete" path="/v1/service-accounts/{service_account_user_id}/api-keys/{api_key_id}" -->
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

    res, err := s.Workspace.DeleteServiceAccountAPIKey(ctx, "<id>", "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `serviceAccountUserID`                                   | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `apiKeyID`                                               | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.DeleteServiceAccountAPIKeyResponse](../../models/operations/deleteserviceaccountapikeyresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditServiceAccountAPIKey

Update an existing API key for a service account

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_service_account_api_key" method="patch" path="/v1/service-accounts/{service_account_user_id}/api-keys/{api_key_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.EditServiceAccountAPIKey(ctx, "<id>", "<id>", &components.BodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatch{
        Name: elevenlabsgo.Pointer("Sneaky Fox"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                             | Type                                                                                                                                                                                                                  | Required                                                                                                                                                                                                              | Description                                                                                                                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                                    | The context to use for the request.                                                                                                                                                                                   |
| `serviceAccountUserID`                                                                                                                                                                                                | `string`                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                    | N/A                                                                                                                                                                                                                   |
| `apiKeyID`                                                                                                                                                                                                            | `string`                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                    | N/A                                                                                                                                                                                                                   |
| `body`                                                                                                                                                                                                                | [*components.BodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatch](../../models/components/bodyeditserviceaccountapikeyv1serviceaccountsserviceaccountuseridapikeysapikeyidpatch.md) | :heavy_minus_sign:                                                                                                                                                                                                    | N/A                                                                                                                                                                                                                   |
| `opts`                                                                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                                                    | The options for this request.                                                                                                                                                                                         |

### Response

**[*operations.EditServiceAccountAPIKeyResponse](../../models/operations/editserviceaccountapikeyresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetWorkspaceAuditLogs

Returns the audit log for the workspace. Requires enterprise tier and the audit_log_read permission.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_workspace_audit_logs" method="get" path="/v1/workspace/audit-logs" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.GetWorkspaceAuditLogs(ctx, operations.GetWorkspaceAuditLogsRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceAuditLogsPageResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                          | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                              | :heavy_check_mark:                                                                                 | The context to use for the request.                                                                |
| `request`                                                                                          | [operations.GetWorkspaceAuditLogsRequest](../../models/operations/getworkspaceauditlogsrequest.md) | :heavy_check_mark:                                                                                 | The request object to use for the request.                                                         |
| `opts`                                                                                             | [][operations.Option](../../models/operations/option.md)                                           | :heavy_minus_sign:                                                                                 | The options for this request.                                                                      |

### Response

**[*operations.GetWorkspaceAuditLogsResponse](../../models/operations/getworkspaceauditlogsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListAuthConnections

Get all auth connections for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="list_auth_connections" method="get" path="/v1/workspace/auth-connections" -->
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

    res, err := s.Workspace.ListAuthConnections(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.ListAuthConnectionsResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.ListAuthConnectionsResponse](../../models/operations/listauthconnectionsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAuthConnection

Create a new OAuth2 auth connection for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="create_auth_connection" method="post" path="/v1/workspace/auth-connections" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.CreateAuthConnection(ctx, operations.CreateCreateAuthConnectionRequestBodyCreatePrivateKeyJWTRequest(
        components.CreatePrivateKeyJWTRequest{
            Name: "<value>",
            Provider: "<value>",
            Issuer: "jcb",
            Audience: "<value>",
            Subject: "<value>",
            SecretKey: "<value>",
        },
    ))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost != nil {
        switch res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.Type {
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeOauth2ClientCredentials:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.OAuth2ClientCredsResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeBasicAuth:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.BasicAuthResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeBearerAuth:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.BearerAuthResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeOauth2Jwt:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.OAuth2JWTResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypePrivateKeyJwt:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.PrivateKeyJWTResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeMtls:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.MTLSAuthResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeCustomHeaderAuth:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.CustomHeaderAuthResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeAPIIntegrationOauth2AuthCode:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.APIIntegrationOAuth2AuthCodeResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeAPIIntegrationOauth2CustomApp:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.APIIntegrationOAuth2CustomAppResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeWhatsappAuth:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.WhatsAppAuthResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeSlackBotAuth:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.SlackBotAuthResponse is populated
            case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeURLSecret:
                // res.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.URLSecretAuthResponse is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                    | :heavy_check_mark:                                                                                       | The context to use for the request.                                                                      |
| `request`                                                                                                | [operations.CreateAuthConnectionRequestBody](../../models/operations/createauthconnectionrequestbody.md) | :heavy_check_mark:                                                                                       | The request object to use for the request.                                                               |
| `opts`                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                 | :heavy_minus_sign:                                                                                       | The options for this request.                                                                            |

### Response

**[*operations.CreateAuthConnectionResponse](../../models/operations/createauthconnectionresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAuthConnection

Delete an auth connection

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_auth_connection" method="delete" path="/v1/workspace/auth-connections/{auth_connection_id}" -->
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

    res, err := s.Workspace.DeleteAuthConnection(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `authConnectionID`                                       | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.DeleteAuthConnectionResponse](../../models/operations/deleteauthconnectionresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateAuthConnection

Update an auth connection

### Example Usage

<!-- UsageSnippet language="go" operationID="update_auth_connection" method="patch" path="/v1/workspace/auth-connections/{auth_connection_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.UpdateAuthConnection(ctx, "<id>", operations.CreateUpdateAuthConnectionRequestBodyUpdateBearerAuthRequest(
        components.UpdateBearerAuthRequest{},
    ))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch != nil {
        switch res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.Type {
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeOauth2ClientCredentials:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.OAuth2ClientCredsResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeBasicAuth:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.BasicAuthResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeBearerAuth:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.BearerAuthResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeOauth2Jwt:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.OAuth2JWTResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypePrivateKeyJwt:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.PrivateKeyJWTResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeMtls:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.MTLSAuthResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeCustomHeaderAuth:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.CustomHeaderAuthResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeAPIIntegrationOauth2AuthCode:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.APIIntegrationOAuth2AuthCodeResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeAPIIntegrationOauth2CustomApp:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.APIIntegrationOAuth2CustomAppResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeWhatsappAuth:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.WhatsAppAuthResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeSlackBotAuth:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.SlackBotAuthResponse is populated
            case operations.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatchTypeURLSecret:
                // res.ResponseUpdateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsAuthConnectionIDPatch.URLSecretAuthResponse is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                    | :heavy_check_mark:                                                                                       | The context to use for the request.                                                                      |
| `authConnectionID`                                                                                       | `string`                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `body`                                                                                                   | [operations.UpdateAuthConnectionRequestBody](../../models/operations/updateauthconnectionrequestbody.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `opts`                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                 | :heavy_minus_sign:                                                                                       | The options for this request.                                                                            |

### Response

**[*operations.UpdateAuthConnectionResponse](../../models/operations/updateauthconnectionresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetWorkspaceServiceAccounts

List all service accounts in the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_workspace_service_accounts" method="get" path="/v1/service-accounts" -->
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

    res, err := s.Workspace.GetWorkspaceServiceAccounts(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceServiceAccountListResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetWorkspaceServiceAccountsResponse](../../models/operations/getworkspaceserviceaccountsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetGroupsEndpoint

Get all groups in the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_groups_endpoint" method="get" path="/v1/workspace/groups" -->
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

    res, err := s.Workspace.GetGroupsEndpoint(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetAllGroupsV1WorkspaceGroupsGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetGroupsEndpointResponse](../../models/operations/getgroupsendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SearchGroups

Searches for user groups in the workspace. Multiple or no groups may be returned.

### Example Usage

<!-- UsageSnippet language="go" operationID="search_groups" method="get" path="/v1/workspace/groups/search" -->
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

    res, err := s.Workspace.SearchGroups(ctx, "<value>")
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseSearchUserGroupsV1WorkspaceGroupsSearchGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `name`                                                   | `string`                                                 | :heavy_check_mark:                                       | Name of the target group.                                |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.SearchGroupsResponse](../../models/operations/searchgroupsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RemoveMember

Removes a member from the specified group. Requires `group_members_manage` permission.

### Example Usage

<!-- UsageSnippet language="go" operationID="remove_member" method="post" path="/v1/workspace/groups/{group_id}/members/remove" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.RemoveMember(ctx, "<id>", components.BodyDeleteMemberFromUserGroupV1WorkspaceGroupsGroupIDMembersRemovePost{
        Email: "Amos.Murphy@yahoo.com",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteWorkspaceGroupMemberResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                              | Type                                                                                                                                                                                   | Required                                                                                                                                                                               | Description                                                                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                     | The context to use for the request.                                                                                                                                                    |
| `groupID`                                                                                                                                                                              | `string`                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                     | The ID of the target group.                                                                                                                                                            |
| `body`                                                                                                                                                                                 | [components.BodyDeleteMemberFromUserGroupV1WorkspaceGroupsGroupIDMembersRemovePost](../../models/components/bodydeletememberfromusergroupv1workspacegroupsgroupidmembersremovepost.md) | :heavy_check_mark:                                                                                                                                                                     | N/A                                                                                                                                                                                    |
| `opts`                                                                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                     | The options for this request.                                                                                                                                                          |

### Response

**[*operations.RemoveMemberResponse](../../models/operations/removememberresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddMember

Adds a member of your workspace to the specified group. Requires `group_members_manage` permission.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_member" method="post" path="/v1/workspace/groups/{group_id}/members" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.AddMember(ctx, "<id>", components.BodyAddMemberToUserGroupV1WorkspaceGroupsGroupIDMembersPost{
        Email: "Devante_Hegmann@hotmail.com",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddWorkspaceGroupMemberResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                        | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                            | :heavy_check_mark:                                                                                                                                               | The context to use for the request.                                                                                                                              |
| `groupID`                                                                                                                                                        | `string`                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The ID of the target group.                                                                                                                                      |
| `body`                                                                                                                                                           | [components.BodyAddMemberToUserGroupV1WorkspaceGroupsGroupIDMembersPost](../../models/components/bodyaddmembertousergroupv1workspacegroupsgroupidmemberspost.md) | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `opts`                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                         | :heavy_minus_sign:                                                                                                                                               | The options for this request.                                                                                                                                    |

### Response

**[*operations.AddMemberResponse](../../models/operations/addmemberresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## InviteUser

Sends an email invitation to join your workspace to the provided email. If the user doesn't have an account they will be prompted to create one. If the user accepts this invite they will be added as a user to your workspace and your subscription using one of your seats. This endpoint may only be called by workspace members with the WORKSPACE_MEMBERS_INVITE permission. If the user is already in the workspace a 400 error will be returned.

### Example Usage

<!-- UsageSnippet language="go" operationID="invite_user" method="post" path="/v1/workspace/invites/add" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.InviteUser(ctx, components.BodyInviteUserV1WorkspaceInvitesAddPost{
        Email: "john.doe@testmail.com",
        GroupIds: []string{
            "group_id_1",
            "group_id_2",
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddWorkspaceInviteResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `request`                                                                                                                | [components.BodyInviteUserV1WorkspaceInvitesAddPost](../../models/components/bodyinviteuserv1workspaceinvitesaddpost.md) | :heavy_check_mark:                                                                                                       | The request object to use for the request.                                                                               |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.InviteUserResponse](../../models/operations/inviteuserresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## InviteUsersBulk

Sends email invitations to join your workspace to the provided emails. Requires all email addresses to be part of a verified domain. If the users don't have an account they will be prompted to create one. If the users accept these invites they will be added as users to your workspace and your subscription using one of your seats. This endpoint may only be called by workspace members with the WORKSPACE_MEMBERS_INVITE permission.

### Example Usage

<!-- UsageSnippet language="go" operationID="invite_users_bulk" method="post" path="/v1/workspace/invites/add-bulk" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.InviteUsersBulk(ctx, components.BodyInviteMultipleUsersV1WorkspaceInvitesAddBulkPost{
        Emails: []string{
            "john.doe@testmail.com",
        },
        GroupIds: []string{
            "group_id_1",
            "group_id_2",
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddWorkspaceInviteResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                          | Type                                                                                                                                               | Required                                                                                                                                           | Description                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                                              | :heavy_check_mark:                                                                                                                                 | The context to use for the request.                                                                                                                |
| `request`                                                                                                                                          | [components.BodyInviteMultipleUsersV1WorkspaceInvitesAddBulkPost](../../models/components/bodyinvitemultipleusersv1workspaceinvitesaddbulkpost.md) | :heavy_check_mark:                                                                                                                                 | The request object to use for the request.                                                                                                         |
| `opts`                                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                                           | :heavy_minus_sign:                                                                                                                                 | The options for this request.                                                                                                                      |

### Response

**[*operations.InviteUsersBulkResponse](../../models/operations/inviteusersbulkresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteInvite

Invalidates an existing email invitation. The invitation will still show up in the inbox it has been delivered to, but activating it to join the workspace won't work. This endpoint may only be called by workspace members with the WORKSPACE_MEMBERS_INVITE permission.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_invite" method="delete" path="/v1/workspace/invites" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.DeleteInvite(ctx, components.BodyDeleteExistingInvitationV1WorkspaceInvitesDelete{
        Email: "john.doe@testmail.com",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteWorkspaceInviteResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                          | Type                                                                                                                                               | Required                                                                                                                                           | Description                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                                              | :heavy_check_mark:                                                                                                                                 | The context to use for the request.                                                                                                                |
| `request`                                                                                                                                          | [components.BodyDeleteExistingInvitationV1WorkspaceInvitesDelete](../../models/components/bodydeleteexistinginvitationv1workspaceinvitesdelete.md) | :heavy_check_mark:                                                                                                                                 | The request object to use for the request.                                                                                                         |
| `opts`                                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                                           | :heavy_minus_sign:                                                                                                                                 | The options for this request.                                                                                                                      |

### Response

**[*operations.DeleteInviteResponse](../../models/operations/deleteinviteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateWorkspaceMember

Updates attributes of a workspace member. Apart from the email identifier, all parameters will remain unchanged unless specified. This endpoint may only be called by workspace administrators.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_workspace_member" method="post" path="/v1/workspace/members" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.UpdateWorkspaceMember(ctx, components.BodyUpdateMemberV1WorkspaceMembersPost{
        Email: "Rebeca88@hotmail.com",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.UpdateWorkspaceMemberResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                              | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                  | :heavy_check_mark:                                                                                                     | The context to use for the request.                                                                                    |
| `request`                                                                                                              | [components.BodyUpdateMemberV1WorkspaceMembersPost](../../models/components/bodyupdatememberv1workspacememberspost.md) | :heavy_check_mark:                                                                                                     | The request object to use for the request.                                                                             |
| `opts`                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                               | :heavy_minus_sign:                                                                                                     | The options for this request.                                                                                          |

### Response

**[*operations.UpdateWorkspaceMemberResponse](../../models/operations/updateworkspacememberresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetResourceMetadata

Gets the metadata of a resource by ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_resource_metadata" method="get" path="/v1/workspace/resources/{resource_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.GetResourceMetadata(ctx, "<id>", components.WorkspaceResourceTypeVoiceCollection)
    if err != nil {
        log.Fatal(err)
    }
    if res.ResourceMetadataResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |
| `resourceID`                                                                         | `string`                                                                             | :heavy_check_mark:                                                                   | The ID of the target resource.                                                       |
| `resourceType`                                                                       | [components.WorkspaceResourceType](../../models/components/workspaceresourcetype.md) | :heavy_check_mark:                                                                   | Resource type of the target resource.                                                |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |

### Response

**[*operations.GetResourceMetadataResponse](../../models/operations/getresourcemetadataresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ShareResourceEndpoint

Grants a role (one of 'admin', 'editor', 'commenter', or 'viewer') on a workspace resource to a user, group, or workspace (service account) API key. This overrides any existing role the target has on the resource. To target a user or service account, pass only the user email; the user must be in your workspace. To target a group, pass only the group id. To target a workspace (service account) API key, pass the api key id; the resource will be shared with the service account associated with that key. You must have admin access to the resource to share it.

### Example Usage

<!-- UsageSnippet language="go" operationID="share_resource_endpoint" method="post" path="/v1/workspace/resources/{resource_id}/share" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.ShareResourceEndpoint(ctx, "<id>", components.BodyShareWorkspaceResourceV1WorkspaceResourcesResourceIDSharePost{
        Role: components.BodyShareWorkspaceResourceV1WorkspaceResourcesResourceIDSharePostRoleViewer,
        ResourceType: components.WorkspaceResourceTypeWorkspaceAuthConnections,
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                    | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                        | :heavy_check_mark:                                                                                                                                                           | The context to use for the request.                                                                                                                                          |
| `resourceID`                                                                                                                                                                 | `string`                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | The ID of the target resource.                                                                                                                                               |
| `body`                                                                                                                                                                       | [components.BodyShareWorkspaceResourceV1WorkspaceResourcesResourceIDSharePost](../../models/components/bodyshareworkspaceresourcev1workspaceresourcesresourceidsharepost.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `opts`                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | The options for this request.                                                                                                                                                |

### Response

**[*operations.ShareResourceEndpointResponse](../../models/operations/shareresourceendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UnshareResourceEndpoint

Removes any existing role on a workspace resource from a user, group, or workspace (service account) API key. To target a user or service account, pass only the user email; the user must be in your workspace. To target a group, pass only the group id. To target a workspace (service account) API key, pass the api key id; the resource will be unshared from the service account associated with that key. You must have admin access to the resource to unshare it. You cannot remove permissions from the user who created the resource.

### Example Usage

<!-- UsageSnippet language="go" operationID="unshare_resource_endpoint" method="post" path="/v1/workspace/resources/{resource_id}/unshare" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.UnshareResourceEndpoint(ctx, "<id>", components.BodyUnshareWorkspaceResourceV1WorkspaceResourcesResourceIDUnsharePost{
        ResourceType: components.WorkspaceResourceTypePronunciationDictionary,
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                            | Type                                                                                                                                                                                 | Required                                                                                                                                                                             | Description                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                | :heavy_check_mark:                                                                                                                                                                   | The context to use for the request.                                                                                                                                                  |
| `resourceID`                                                                                                                                                                         | `string`                                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                   | The ID of the target resource.                                                                                                                                                       |
| `body`                                                                                                                                                                               | [components.BodyUnshareWorkspaceResourceV1WorkspaceResourcesResourceIDUnsharePost](../../models/components/bodyunshareworkspaceresourcev1workspaceresourcesresourceidunsharepost.md) | :heavy_check_mark:                                                                                                                                                                   | N/A                                                                                                                                                                                  |
| `opts`                                                                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                                                                             | :heavy_minus_sign:                                                                                                                                                                   | The options for this request.                                                                                                                                                        |

### Response

**[*operations.UnshareResourceEndpointResponse](../../models/operations/unshareresourceendpointresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetWorkspaceWebhooks

List all webhooks for a workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_workspace_webhooks_route" method="get" path="/v1/workspace/webhooks" -->
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

    res, err := s.Workspace.GetWorkspaceWebhooks(ctx, elevenlabsgo.Pointer(false))
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceWebhookListResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `ctx`                                                                  | [context.Context](https://pkg.go.dev/context#Context)                  | :heavy_check_mark:                                                     | The context to use for the request.                                    |                                                                        |
| `includeUsages`                                                        | `*bool`                                                                | :heavy_minus_sign:                                                     | Whether to include active usages of the webhook, only usable by admins | false                                                                  |
| `opts`                                                                 | [][operations.Option](../../models/operations/option.md)               | :heavy_minus_sign:                                                     | The options for this request.                                          |                                                                        |

### Response

**[*operations.GetWorkspaceWebhooksRouteResponse](../../models/operations/getworkspacewebhooksrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateWorkspaceWebhook

Create a new webhook for the workspace with the specified authentication type.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_workspace_webhook_route" method="post" path="/v1/workspace/webhooks" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.CreateWorkspaceWebhook(ctx, components.BodyCreateWorkspaceWebhookV1WorkspaceWebhooksPost{
        Settings: components.WebhookHMACSettings{
            Name: "<value>",
            WebhookURL: "https://alarmed-median.net/",
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceCreateWebhookResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                    | Type                                                                                                                                         | Required                                                                                                                                     | Description                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                        | :heavy_check_mark:                                                                                                                           | The context to use for the request.                                                                                                          |
| `request`                                                                                                                                    | [components.BodyCreateWorkspaceWebhookV1WorkspaceWebhooksPost](../../models/components/bodycreateworkspacewebhookv1workspacewebhookspost.md) | :heavy_check_mark:                                                                                                                           | The request object to use for the request.                                                                                                   |
| `opts`                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                     | :heavy_minus_sign:                                                                                                                           | The options for this request.                                                                                                                |

### Response

**[*operations.CreateWorkspaceWebhookRouteResponse](../../models/operations/createworkspacewebhookrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## EditWorkspaceWebhook

Update the specified workspace webhook

### Example Usage

<!-- UsageSnippet language="go" operationID="edit_workspace_webhook_route" method="patch" path="/v1/workspace/webhooks/{webhook_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Workspace.EditWorkspaceWebhook(ctx, "G007vmtq9uWYl7SUW9zGS8GZZa1K", components.BodyUpdateWorkspaceWebhookV1WorkspaceWebhooksWebhookIDPatch{
        IsDisabled: true,
        Name: "My Callback Webhook",
        RetryEnabled: elevenlabsgo.Pointer(true),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.PatchWorkspaceWebhookResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                        | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      | Example                                                                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                            | :heavy_check_mark:                                                                                                                                               | The context to use for the request.                                                                                                                              |                                                                                                                                                                  |
| `webhookID`                                                                                                                                                      | `string`                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The unique ID for the webhook                                                                                                                                    | G007vmtq9uWYl7SUW9zGS8GZZa1K                                                                                                                                     |
| `body`                                                                                                                                                           | [components.BodyUpdateWorkspaceWebhookV1WorkspaceWebhooksWebhookIDPatch](../../models/components/bodyupdateworkspacewebhookv1workspacewebhookswebhookidpatch.md) | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |                                                                                                                                                                  |
| `opts`                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                         | :heavy_minus_sign:                                                                                                                                               | The options for this request.                                                                                                                                    |                                                                                                                                                                  |

### Response

**[*operations.EditWorkspaceWebhookRouteResponse](../../models/operations/editworkspacewebhookrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteWorkspaceWebhook

Delete the specified workspace webhook

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_workspace_webhook_route" method="delete" path="/v1/workspace/webhooks/{webhook_id}" -->
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

    res, err := s.Workspace.DeleteWorkspaceWebhook(ctx, "G007vmtq9uWYl7SUW9zGS8GZZa1K")
    if err != nil {
        log.Fatal(err)
    }
    if res.DeleteWorkspaceWebhookResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `webhookID`                                              | `string`                                                 | :heavy_check_mark:                                       | The unique ID for the webhook                            | G007vmtq9uWYl7SUW9zGS8GZZa1K                             |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteWorkspaceWebhookRouteResponse](../../models/operations/deleteworkspacewebhookrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |