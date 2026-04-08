# SourceContext


## Supported Types

### MusicExploreSongSourceContext

```go
sourceContext := components.CreateSourceContextMusicExploreSong(components.MusicExploreSongSourceContext{/* values here */})
```

### SfxSourceContext

```go
sourceContext := components.CreateSourceContextSfx(components.SfxSourceContext{/* values here */})
```

### SongSourceContext

```go
sourceContext := components.CreateSourceContextSong(components.SongSourceContext{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch sourceContext.Type {
	case components.SourceContextTypeMusicExploreSong:
		// sourceContext.MusicExploreSongSourceContext is populated
	case components.SourceContextTypeSfx:
		// sourceContext.SfxSourceContext is populated
	case components.SourceContextTypeSong:
		// sourceContext.SongSourceContext is populated
}
```
