# SourceUnion2

The source content for the Podcast.


## Supported Types

### PodcastTextSource

```go
sourceUnion2 := components.CreateSourceUnion2PodcastTextSource(components.PodcastTextSource{/* values here */})
```

### PodcastURLSource

```go
sourceUnion2 := components.CreateSourceUnion2PodcastURLSource(components.PodcastURLSource{/* values here */})
```

### 

```go
sourceUnion2 := components.CreateSourceUnion2ArrayOfSourceUnion1([]components.SourceUnion1{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch sourceUnion2.Type {
	case components.SourceUnion2TypePodcastTextSource:
		// sourceUnion2.PodcastTextSource is populated
	case components.SourceUnion2TypePodcastURLSource:
		// sourceUnion2.PodcastURLSource is populated
	case components.SourceUnion2TypeArrayOfSourceUnion1:
		// sourceUnion2.ArrayOfSourceUnion1 is populated
}
```
