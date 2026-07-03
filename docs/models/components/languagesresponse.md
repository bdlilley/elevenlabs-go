# LanguagesResponse


## Supported Types

### PairedLanguagesResponse

```go
languagesResponse := components.CreateLanguagesResponsePair(components.PairedLanguagesResponse{/* values here */})
```

### SingleLanguagesResponse

```go
languagesResponse := components.CreateLanguagesResponseSingle(components.SingleLanguagesResponse{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch languagesResponse.Type {
	case components.LanguagesResponseTypePair:
		// languagesResponse.PairedLanguagesResponse is populated
	case components.LanguagesResponseTypeSingle:
		// languagesResponse.SingleLanguagesResponse is populated
}
```
