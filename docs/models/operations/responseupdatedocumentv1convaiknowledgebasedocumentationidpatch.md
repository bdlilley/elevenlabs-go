# ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch

Successful Response


## Supported Types

### GetKnowledgeBaseURLResponseModel

```go
responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch := operations.CreateResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchURLObj(components.GetKnowledgeBaseURLResponseModel{/* values here */})
```

### GetKnowledgeBaseFileResponseModel

```go
responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch := operations.CreateResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchFile(components.GetKnowledgeBaseFileResponseModel{/* values here */})
```

### GetKnowledgeBaseTextResponseModel

```go
responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch := operations.CreateResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchText(components.GetKnowledgeBaseTextResponseModel{/* values here */})
```

### GetKnowledgeBaseFolderResponseModel

```go
responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch := operations.CreateResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchFolder(components.GetKnowledgeBaseFolderResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.Type {
	case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeURLObj:
		// responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseURLResponseModel is populated
	case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeFile:
		// responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseFileResponseModel is populated
	case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeText:
		// responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseTextResponseModel is populated
	case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeFolder:
		// responseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseFolderResponseModel is populated
}
```
