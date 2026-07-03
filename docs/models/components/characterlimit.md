# CharacterLimit

The character limit of the XI API key. If provided this will limit the usage of this api key to n characters per month where n is the chosen value. Requests that incur charges will fail after reaching this monthly limit.


## Supported Types

### 

```go
characterLimit := components.CreateCharacterLimitInteger(int64{/* values here */})
```

### 

```go
characterLimit := components.CreateCharacterLimitStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch characterLimit.Type {
	case components.CharacterLimitTypeInteger:
		// characterLimit.Integer is populated
	case components.CharacterLimitTypeStr:
		// characterLimit.Str is populated
}
```
