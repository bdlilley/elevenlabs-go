# Dependencies3


## Supported Types

### 

```go
dependencies3 := components.CreateDependencies3ArrayOfDependencies1([]components.Dependencies1{/* values here */})
```

### 

```go
dependencies3 := components.CreateDependencies3ArrayOfDependencies2([]components.Dependencies2{/* values here */})
```

### 

```go
dependencies3 := components.CreateDependencies3ArrayOfDependentPhoneNumberIdentifier([]components.DependentPhoneNumberIdentifier{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch dependencies3.Type {
	case components.Dependencies3TypeArrayOfDependencies1:
		// dependencies3.ArrayOfDependencies1 is populated
	case components.Dependencies3TypeArrayOfDependencies2:
		// dependencies3.ArrayOfDependencies2 is populated
	case components.Dependencies3TypeArrayOfDependentPhoneNumberIdentifier:
		// dependencies3.ArrayOfDependentPhoneNumberIdentifier is populated
}
```
