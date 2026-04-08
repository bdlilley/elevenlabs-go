# KnowledgeBaseContentSearchResultDocument


## Supported Types

### GetKnowledgeBaseSummaryFileResponseModel

```go
knowledgeBaseContentSearchResultDocument := components.CreateKnowledgeBaseContentSearchResultDocumentFile(components.GetKnowledgeBaseSummaryFileResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryFolderResponseModel

```go
knowledgeBaseContentSearchResultDocument := components.CreateKnowledgeBaseContentSearchResultDocumentFolder(components.GetKnowledgeBaseSummaryFolderResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryTextResponseModel

```go
knowledgeBaseContentSearchResultDocument := components.CreateKnowledgeBaseContentSearchResultDocumentText(components.GetKnowledgeBaseSummaryTextResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryURLResponseModel

```go
knowledgeBaseContentSearchResultDocument := components.CreateKnowledgeBaseContentSearchResultDocumentURLObj(components.GetKnowledgeBaseSummaryURLResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch knowledgeBaseContentSearchResultDocument.Type {
	case components.KnowledgeBaseContentSearchResultDocumentTypeFile:
		// knowledgeBaseContentSearchResultDocument.GetKnowledgeBaseSummaryFileResponseModel is populated
	case components.KnowledgeBaseContentSearchResultDocumentTypeFolder:
		// knowledgeBaseContentSearchResultDocument.GetKnowledgeBaseSummaryFolderResponseModel is populated
	case components.KnowledgeBaseContentSearchResultDocumentTypeText:
		// knowledgeBaseContentSearchResultDocument.GetKnowledgeBaseSummaryTextResponseModel is populated
	case components.KnowledgeBaseContentSearchResultDocumentTypeURLObj:
		// knowledgeBaseContentSearchResultDocument.GetKnowledgeBaseSummaryURLResponseModel is populated
}
```
