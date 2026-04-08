# GetOrCreateRagIndexesResponseBody


## Supported Types

### RAGIndexBatchSuccessfulResponseModel

```go
getOrCreateRagIndexesResponseBody := operations.CreateGetOrCreateRagIndexesResponseBodySuccess(components.RAGIndexBatchSuccessfulResponseModel{/* values here */})
```

### BatchFailureResponseModel

```go
getOrCreateRagIndexesResponseBody := operations.CreateGetOrCreateRagIndexesResponseBodyFailure(components.BatchFailureResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getOrCreateRagIndexesResponseBody.Type {
	case operations.GetOrCreateRagIndexesResponseBodyTypeSuccess:
		// getOrCreateRagIndexesResponseBody.RAGIndexBatchSuccessfulResponseModel is populated
	case operations.GetOrCreateRagIndexesResponseBodyTypeFailure:
		// getOrCreateRagIndexesResponseBody.BatchFailureResponseModel is populated
}
```
