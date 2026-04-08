# APIIntegrationWebhookOverridesRequestHeaders


## Supported Types

### 

```go
apiIntegrationWebhookOverridesRequestHeaders := components.CreateAPIIntegrationWebhookOverridesRequestHeadersStr(string{/* values here */})
```

### ConvAIDynamicVariable

```go
apiIntegrationWebhookOverridesRequestHeaders := components.CreateAPIIntegrationWebhookOverridesRequestHeadersConvAIDynamicVariable(components.ConvAIDynamicVariable{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch apiIntegrationWebhookOverridesRequestHeaders.Type {
	case components.APIIntegrationWebhookOverridesRequestHeadersTypeStr:
		// apiIntegrationWebhookOverridesRequestHeaders.Str is populated
	case components.APIIntegrationWebhookOverridesRequestHeadersTypeConvAIDynamicVariable:
		// apiIntegrationWebhookOverridesRequestHeaders.ConvAIDynamicVariable is populated
}
```
