# ListAuthConnectionsResponseAuthConnection

The type of auth connection config


## Supported Types

### APIIntegrationOAuth2AuthCodeResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionAPIIntegrationOauth2AuthCode(components.APIIntegrationOAuth2AuthCodeResponse{/* values here */})
```

### BasicAuthResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionBasicAuth(components.BasicAuthResponse{/* values here */})
```

### BearerAuthResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionBearerAuth(components.BearerAuthResponse{/* values here */})
```

### CustomHeaderAuthResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionCustomHeaderAuth(components.CustomHeaderAuthResponse{/* values here */})
```

### MTLSAuthResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionMtls(components.MTLSAuthResponse{/* values here */})
```

### OAuth2ClientCredsResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionOauth2ClientCredentials(components.OAuth2ClientCredsResponse{/* values here */})
```

### OAuth2JWTResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionOauth2Jwt(components.OAuth2JWTResponse{/* values here */})
```

### PrivateKeyJWTResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionPrivateKeyJwt(components.PrivateKeyJWTResponse{/* values here */})
```

### WhatsAppAuthResponse

```go
listAuthConnectionsResponseAuthConnection := components.CreateListAuthConnectionsResponseAuthConnectionWhatsappAuth(components.WhatsAppAuthResponse{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch listAuthConnectionsResponseAuthConnection.Type {
	case components.ListAuthConnectionsResponseAuthConnectionTypeAPIIntegrationOauth2AuthCode:
		// listAuthConnectionsResponseAuthConnection.APIIntegrationOAuth2AuthCodeResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeBasicAuth:
		// listAuthConnectionsResponseAuthConnection.BasicAuthResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeBearerAuth:
		// listAuthConnectionsResponseAuthConnection.BearerAuthResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeCustomHeaderAuth:
		// listAuthConnectionsResponseAuthConnection.CustomHeaderAuthResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeMtls:
		// listAuthConnectionsResponseAuthConnection.MTLSAuthResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeOauth2ClientCredentials:
		// listAuthConnectionsResponseAuthConnection.OAuth2ClientCredsResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeOauth2Jwt:
		// listAuthConnectionsResponseAuthConnection.OAuth2JWTResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypePrivateKeyJwt:
		// listAuthConnectionsResponseAuthConnection.PrivateKeyJWTResponse is populated
	case components.ListAuthConnectionsResponseAuthConnectionTypeWhatsappAuth:
		// listAuthConnectionsResponseAuthConnection.WhatsAppAuthResponse is populated
	default:
		// Unknown type - use listAuthConnectionsResponseAuthConnection.GetUnknownRaw() for raw JSON
}
```
