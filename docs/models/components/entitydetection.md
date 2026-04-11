# EntityDetection

Detect entities in the transcript. Can be 'all' to detect all entities, a single entity type or category string, or a list of entity types/categories. Categories include 'pii', 'phi', 'pci', 'other', 'offensive_language'. When enabled, detected entities will be returned in the 'entities' field with their text, type, and character positions. Usage of this parameter will incur an additional 30% surcharge on the base transcription cost.


## Supported Types

### 

```go
entityDetection := components.CreateEntityDetectionStr(string{/* values here */})
```

### 

```go
entityDetection := components.CreateEntityDetectionArrayOfStr([]string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch entityDetection.Type {
	case components.EntityDetectionTypeStr:
		// entityDetection.Str is populated
	case components.EntityDetectionTypeArrayOfStr:
		// entityDetection.ArrayOfStr is populated
}
```
