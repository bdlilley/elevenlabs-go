# SourceUnion1


## Supported Types

### PodcastTextSource

```go
sourceUnion1 := components.CreateSourceUnion1Text(components.PodcastTextSource{/* values here */})
```

### PodcastURLSource

```go
sourceUnion1 := components.CreateSourceUnion1URLObj(components.PodcastURLSource{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch sourceUnion1.Type {
	case components.SourceUnion1TypeText:
		// sourceUnion1.PodcastTextSource is populated
	case components.SourceUnion1TypeURLObj:
		// sourceUnion1.PodcastURLSource is populated
}
```
