# ThirdPartyDisableAllowed

Whether the holder of this key may disable it via the self-disable endpoint. On create, omit or pass null to use the workspace's default (enabled for non-Enterprise plans, disabled for Enterprise plans). On update, omit to leave it unchanged, or pass "clear" to reset it to the workspace default. Only honored for workspaces with self-disable access enabled.


## Supported Types

### 

```go
thirdPartyDisableAllowed := components.CreateThirdPartyDisableAllowedBoolean(bool{/* values here */})
```

### ThirdPartyDisableAllowedEnum

```go
thirdPartyDisableAllowed := components.CreateThirdPartyDisableAllowedThirdPartyDisableAllowedEnum(components.ThirdPartyDisableAllowedEnum{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch thirdPartyDisableAllowed.Type {
	case components.ThirdPartyDisableAllowedTypeBoolean:
		// thirdPartyDisableAllowed.Boolean is populated
	case components.ThirdPartyDisableAllowedTypeThirdPartyDisableAllowedEnum:
		// thirdPartyDisableAllowed.ThirdPartyDisableAllowedEnum is populated
}
```
