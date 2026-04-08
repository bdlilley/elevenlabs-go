# ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost

The type of auth connection config


## Supported Types

### OAuth2ClientCredsResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostOauth2ClientCredentials(components.OAuth2ClientCredsResponse{/* values here */})
```

### BasicAuthResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostBasicAuth(components.BasicAuthResponse{/* values here */})
```

### BearerAuthResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostBearerAuth(components.BearerAuthResponse{/* values here */})
```

### OAuth2JWTResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostOauth2Jwt(components.OAuth2JWTResponse{/* values here */})
```

### PrivateKeyJWTResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostPrivateKeyJwt(components.PrivateKeyJWTResponse{/* values here */})
```

### MTLSAuthResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostMtls(components.MTLSAuthResponse{/* values here */})
```

### CustomHeaderAuthResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostCustomHeaderAuth(components.CustomHeaderAuthResponse{/* values here */})
```

### APIIntegrationOAuth2AuthCodeResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostAPIIntegrationOauth2AuthCode(components.APIIntegrationOAuth2AuthCodeResponse{/* values here */})
```

### WhatsAppAuthResponse

```go
responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost := operations.CreateResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostWhatsappAuth(components.WhatsAppAuthResponse{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.Type {
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeOauth2ClientCredentials:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.OAuth2ClientCredsResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeBasicAuth:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.BasicAuthResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeBearerAuth:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.BearerAuthResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeOauth2Jwt:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.OAuth2JWTResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypePrivateKeyJwt:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.PrivateKeyJWTResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeMtls:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.MTLSAuthResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeCustomHeaderAuth:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.CustomHeaderAuthResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeAPIIntegrationOauth2AuthCode:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.APIIntegrationOAuth2AuthCodeResponse is populated
	case operations.ResponseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPostTypeWhatsappAuth:
		// responseCreateWorkspaceAuthConnectionV1WorkspaceAuthConnectionsPost.WhatsAppAuthResponse is populated
}
```
