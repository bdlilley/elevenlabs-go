# TemplateParam


## Supported Types

### WhatsAppTemplateBodyComponentParams

```go
templateParam := components.CreateTemplateParamBody(components.WhatsAppTemplateBodyComponentParams{/* values here */})
```

### WhatsAppTemplateButtonComponentParams

```go
templateParam := components.CreateTemplateParamButton(components.WhatsAppTemplateButtonComponentParams{/* values here */})
```

### WhatsAppTemplateHeaderComponentParams

```go
templateParam := components.CreateTemplateParamHeader(components.WhatsAppTemplateHeaderComponentParams{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch templateParam.Type {
	case components.TemplateParamTypeBody:
		// templateParam.WhatsAppTemplateBodyComponentParams is populated
	case components.TemplateParamTypeButton:
		// templateParam.WhatsAppTemplateButtonComponentParams is populated
	case components.TemplateParamTypeHeader:
		// templateParam.WhatsAppTemplateHeaderComponentParams is populated
}
```
