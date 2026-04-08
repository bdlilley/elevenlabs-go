# ExportOptions


## Supported Types

### DocxExportOptions

```go
exportOptions := components.CreateExportOptionsDocx(components.DocxExportOptions{/* values here */})
```

### HTMLExportOptions

```go
exportOptions := components.CreateExportOptionsHTML(components.HTMLExportOptions{/* values here */})
```

### PdfExportOptions

```go
exportOptions := components.CreateExportOptionsPdf(components.PdfExportOptions{/* values here */})
```

### SegmentedJSONExportOptions

```go
exportOptions := components.CreateExportOptionsSegmentedJSON(components.SegmentedJSONExportOptions{/* values here */})
```

### SrtExportOptions

```go
exportOptions := components.CreateExportOptionsSrt(components.SrtExportOptions{/* values here */})
```

### TxtExportOptions

```go
exportOptions := components.CreateExportOptionsTxt(components.TxtExportOptions{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch exportOptions.Type {
	case components.ExportOptionsTypeDocx:
		// exportOptions.DocxExportOptions is populated
	case components.ExportOptionsTypeHTML:
		// exportOptions.HTMLExportOptions is populated
	case components.ExportOptionsTypePdf:
		// exportOptions.PdfExportOptions is populated
	case components.ExportOptionsTypeSegmentedJSON:
		// exportOptions.SegmentedJSONExportOptions is populated
	case components.ExportOptionsTypeSrt:
		// exportOptions.SrtExportOptions is populated
	case components.ExportOptionsTypeTxt:
		// exportOptions.TxtExportOptions is populated
}
```
