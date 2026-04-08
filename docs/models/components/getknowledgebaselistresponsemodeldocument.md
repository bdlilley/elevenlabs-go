# GetKnowledgeBaseListResponseModelDocument


## Supported Types

### GetKnowledgeBaseSummaryFileResponseModel

```go
getKnowledgeBaseListResponseModelDocument := components.CreateGetKnowledgeBaseListResponseModelDocumentFile(components.GetKnowledgeBaseSummaryFileResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryFolderResponseModel

```go
getKnowledgeBaseListResponseModelDocument := components.CreateGetKnowledgeBaseListResponseModelDocumentFolder(components.GetKnowledgeBaseSummaryFolderResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryTextResponseModel

```go
getKnowledgeBaseListResponseModelDocument := components.CreateGetKnowledgeBaseListResponseModelDocumentText(components.GetKnowledgeBaseSummaryTextResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryURLResponseModel

```go
getKnowledgeBaseListResponseModelDocument := components.CreateGetKnowledgeBaseListResponseModelDocumentURLObj(components.GetKnowledgeBaseSummaryURLResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getKnowledgeBaseListResponseModelDocument.Type {
	case components.GetKnowledgeBaseListResponseModelDocumentTypeFile:
		// getKnowledgeBaseListResponseModelDocument.GetKnowledgeBaseSummaryFileResponseModel is populated
	case components.GetKnowledgeBaseListResponseModelDocumentTypeFolder:
		// getKnowledgeBaseListResponseModelDocument.GetKnowledgeBaseSummaryFolderResponseModel is populated
	case components.GetKnowledgeBaseListResponseModelDocumentTypeText:
		// getKnowledgeBaseListResponseModelDocument.GetKnowledgeBaseSummaryTextResponseModel is populated
	case components.GetKnowledgeBaseListResponseModelDocumentTypeURLObj:
		// getKnowledgeBaseListResponseModelDocument.GetKnowledgeBaseSummaryURLResponseModel is populated
	default:
		// Unknown type - use getKnowledgeBaseListResponseModelDocument.GetUnknownRaw() for raw JSON
}
```
