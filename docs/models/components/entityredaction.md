# EntityRedaction

Redact entities from the transcript text. Accepts the same format as entity_detection: 'all', a category ('pii', 'phi'), or specific entity types. Must be a subset of entity_detection. When redaction is enabled, the entities field will not be returned.


## Supported Types

### 

```go
entityRedaction := components.CreateEntityRedactionStr(string{/* values here */})
```

### 

```go
entityRedaction := components.CreateEntityRedactionArrayOfStr([]string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch entityRedaction.Type {
	case components.EntityRedactionTypeStr:
		// entityRedaction.Str is populated
	case components.EntityRedactionTypeArrayOfStr:
		// entityRedaction.ArrayOfStr is populated
}
```
