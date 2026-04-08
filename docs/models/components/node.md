# Node


## Supported Types

### ChapterContentBlockTtsNodeResponseModel

```go
node := components.CreateNodeTtsNode(components.ChapterContentBlockTtsNodeResponseModel{/* values here */})
```

### ChapterContentBlockExtendableNodeResponseModel

```go
node := components.CreateNodeOther(components.ChapterContentBlockExtendableNodeResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch node.Type {
	case components.NodeTypeTtsNode:
		// node.ChapterContentBlockTtsNodeResponseModel is populated
	case components.NodeTypeOther:
		// node.ChapterContentBlockExtendableNodeResponseModel is populated
}
```
