# Chunk


## Supported Types

### GenerationChunkInput

```go
chunk := components.CreateChunkGenerationChunkInput(components.GenerationChunkInput{/* values here */})
```

### AudioRefChunk

```go
chunk := components.CreateChunkAudioRefChunk(components.AudioRefChunk{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch chunk.Type {
	case components.ChunkTypeGenerationChunkInput:
		// chunk.GenerationChunkInput is populated
	case components.ChunkTypeAudioRefChunk:
		// chunk.AudioRefChunk is populated
}
```
