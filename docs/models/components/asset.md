# Asset


## Supported Types

### ProjectVideoResponseModel

```go
asset := components.CreateAssetProjectVideoResponseModel(components.ProjectVideoResponseModel{/* values here */})
```

### ProjectExternalAudioResponseModel

```go
asset := components.CreateAssetProjectExternalAudioResponseModel(components.ProjectExternalAudioResponseModel{/* values here */})
```

### ProjectImageResponseModel

```go
asset := components.CreateAssetProjectImageResponseModel(components.ProjectImageResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch asset.Type {
	case components.AssetTypeProjectVideoResponseModel:
		// asset.ProjectVideoResponseModel is populated
	case components.AssetTypeProjectExternalAudioResponseModel:
		// asset.ProjectExternalAudioResponseModel is populated
	case components.AssetTypeProjectImageResponseModel:
		// asset.ProjectImageResponseModel is populated
}
```
