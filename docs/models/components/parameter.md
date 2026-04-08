# Parameter


## Supported Types

### WhatsAppTemplateDocumentParam

```go
parameter := components.CreateParameterDocument(components.WhatsAppTemplateDocumentParam{/* values here */})
```

### WhatsAppTemplateImageParam

```go
parameter := components.CreateParameterImage(components.WhatsAppTemplateImageParam{/* values here */})
```

### WhatsAppTemplateLocationParam

```go
parameter := components.CreateParameterLocation(components.WhatsAppTemplateLocationParam{/* values here */})
```

### WhatsAppTemplateTextParam

```go
parameter := components.CreateParameterText(components.WhatsAppTemplateTextParam{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch parameter.Type {
	case components.ParameterTypeDocument:
		// parameter.WhatsAppTemplateDocumentParam is populated
	case components.ParameterTypeImage:
		// parameter.WhatsAppTemplateImageParam is populated
	case components.ParameterTypeLocation:
		// parameter.WhatsAppTemplateLocationParam is populated
	case components.ParameterTypeText:
		// parameter.WhatsAppTemplateTextParam is populated
}
```
