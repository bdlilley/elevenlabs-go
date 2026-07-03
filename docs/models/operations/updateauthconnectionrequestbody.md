# UpdateAuthConnectionRequestBody

Updated auth connection fields


## Supported Types

### UpdateOAuth2ClientCredsRequest

```go
updateAuthConnectionRequestBody := operations.CreateUpdateAuthConnectionRequestBodyUpdateOAuth2ClientCredsRequest(components.UpdateOAuth2ClientCredsRequest{/* values here */})
```

### UpdateBasicAuthRequest

```go
updateAuthConnectionRequestBody := operations.CreateUpdateAuthConnectionRequestBodyUpdateBasicAuthRequest(components.UpdateBasicAuthRequest{/* values here */})
```

### UpdateBearerAuthRequest

```go
updateAuthConnectionRequestBody := operations.CreateUpdateAuthConnectionRequestBodyUpdateBearerAuthRequest(components.UpdateBearerAuthRequest{/* values here */})
```

### UpdateOAuth2JWTRequest

```go
updateAuthConnectionRequestBody := operations.CreateUpdateAuthConnectionRequestBodyUpdateOAuth2JWTRequest(components.UpdateOAuth2JWTRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch updateAuthConnectionRequestBody.Type {
	case operations.UpdateAuthConnectionRequestBodyTypeUpdateOAuth2ClientCredsRequest:
		// updateAuthConnectionRequestBody.UpdateOAuth2ClientCredsRequest is populated
	case operations.UpdateAuthConnectionRequestBodyTypeUpdateBasicAuthRequest:
		// updateAuthConnectionRequestBody.UpdateBasicAuthRequest is populated
	case operations.UpdateAuthConnectionRequestBodyTypeUpdateBearerAuthRequest:
		// updateAuthConnectionRequestBody.UpdateBearerAuthRequest is populated
	case operations.UpdateAuthConnectionRequestBodyTypeUpdateOAuth2JWTRequest:
		// updateAuthConnectionRequestBody.UpdateOAuth2JWTRequest is populated
}
```
