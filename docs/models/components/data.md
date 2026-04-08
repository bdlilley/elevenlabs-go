# Data


## Supported Types

### GetKnowledgeBaseSummaryFileResponseModel

```go
data := components.CreateDataFile(components.GetKnowledgeBaseSummaryFileResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryFolderResponseModel

```go
data := components.CreateDataFolder(components.GetKnowledgeBaseSummaryFolderResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryTextResponseModel

```go
data := components.CreateDataText(components.GetKnowledgeBaseSummaryTextResponseModel{/* values here */})
```

### GetKnowledgeBaseSummaryURLResponseModel

```go
data := components.CreateDataURLObj(components.GetKnowledgeBaseSummaryURLResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch data.Type {
	case components.DataTypeFile:
		// data.GetKnowledgeBaseSummaryFileResponseModel is populated
	case components.DataTypeFolder:
		// data.GetKnowledgeBaseSummaryFolderResponseModel is populated
	case components.DataTypeText:
		// data.GetKnowledgeBaseSummaryTextResponseModel is populated
	case components.DataTypeURLObj:
		// data.GetKnowledgeBaseSummaryURLResponseModel is populated
	default:
		// Unknown type - use data.GetUnknownRaw() for raw JSON
}
```
