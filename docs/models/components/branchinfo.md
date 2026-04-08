# BranchInfo


## Supported Types

### TransferBranchInfoDefaultingToMain

```go
branchInfo := components.CreateBranchInfoDefaultingToMain(components.TransferBranchInfoDefaultingToMain{/* values here */})
```

### TransferBranchInfoTrafficSplit

```go
branchInfo := components.CreateBranchInfoTrafficSplit(components.TransferBranchInfoTrafficSplit{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch branchInfo.Type {
	case components.BranchInfoTypeDefaultingToMain:
		// branchInfo.TransferBranchInfoDefaultingToMain is populated
	case components.BranchInfoTypeTrafficSplit:
		// branchInfo.TransferBranchInfoTrafficSplit is populated
}
```
