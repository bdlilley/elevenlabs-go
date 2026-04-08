# CreateAuthConnectionRequestBody

Auth connection to create


## Supported Types

### CreateOAuth2ClientCredsRequest

```go
createAuthConnectionRequestBody := operations.CreateCreateAuthConnectionRequestBodyCreateOAuth2ClientCredsRequest(components.CreateOAuth2ClientCredsRequest{/* values here */})
```

### CreateCustomHeaderAuthRequest

```go
createAuthConnectionRequestBody := operations.CreateCreateAuthConnectionRequestBodyCreateCustomHeaderAuthRequest(components.CreateCustomHeaderAuthRequest{/* values here */})
```

### CreateBasicAuthRequest

```go
createAuthConnectionRequestBody := operations.CreateCreateAuthConnectionRequestBodyCreateBasicAuthRequest(components.CreateBasicAuthRequest{/* values here */})
```

### CreateOAuth2JWTRequest

```go
createAuthConnectionRequestBody := operations.CreateCreateAuthConnectionRequestBodyCreateOAuth2JWTRequest(components.CreateOAuth2JWTRequest{/* values here */})
```

### CreatePrivateKeyJWTRequest

```go
createAuthConnectionRequestBody := operations.CreateCreateAuthConnectionRequestBodyCreatePrivateKeyJWTRequest(components.CreatePrivateKeyJWTRequest{/* values here */})
```

### CreateMTLSAuthRequest

```go
createAuthConnectionRequestBody := operations.CreateCreateAuthConnectionRequestBodyCreateMTLSAuthRequest(components.CreateMTLSAuthRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch createAuthConnectionRequestBody.Type {
	case operations.CreateAuthConnectionRequestBodyTypeCreateOAuth2ClientCredsRequest:
		// createAuthConnectionRequestBody.CreateOAuth2ClientCredsRequest is populated
	case operations.CreateAuthConnectionRequestBodyTypeCreateCustomHeaderAuthRequest:
		// createAuthConnectionRequestBody.CreateCustomHeaderAuthRequest is populated
	case operations.CreateAuthConnectionRequestBodyTypeCreateBasicAuthRequest:
		// createAuthConnectionRequestBody.CreateBasicAuthRequest is populated
	case operations.CreateAuthConnectionRequestBodyTypeCreateOAuth2JWTRequest:
		// createAuthConnectionRequestBody.CreateOAuth2JWTRequest is populated
	case operations.CreateAuthConnectionRequestBodyTypeCreatePrivateKeyJWTRequest:
		// createAuthConnectionRequestBody.CreatePrivateKeyJWTRequest is populated
	case operations.CreateAuthConnectionRequestBodyTypeCreateMTLSAuthRequest:
		// createAuthConnectionRequestBody.CreateMTLSAuthRequest is populated
}
```
