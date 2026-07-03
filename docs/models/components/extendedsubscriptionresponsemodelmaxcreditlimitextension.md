# ExtendedSubscriptionResponseModelMaxCreditLimitExtension

Maximum number of credits that the credit limit can be exceeded by. Managed by the workspace admin. `"unlimited"` means no cap, `0` means usage-based billing is disabled.


## Supported Types

### 

```go
extendedSubscriptionResponseModelMaxCreditLimitExtension := components.CreateExtendedSubscriptionResponseModelMaxCreditLimitExtensionInteger(int64{/* values here */})
```

### 

```go
extendedSubscriptionResponseModelMaxCreditLimitExtension := components.CreateExtendedSubscriptionResponseModelMaxCreditLimitExtensionStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch extendedSubscriptionResponseModelMaxCreditLimitExtension.Type {
	case components.ExtendedSubscriptionResponseModelMaxCreditLimitExtensionTypeInteger:
		// extendedSubscriptionResponseModelMaxCreditLimitExtension.Integer is populated
	case components.ExtendedSubscriptionResponseModelMaxCreditLimitExtensionTypeStr:
		// extendedSubscriptionResponseModelMaxCreditLimitExtension.Str is populated
}
```
