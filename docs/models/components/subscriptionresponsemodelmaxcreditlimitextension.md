# SubscriptionResponseModelMaxCreditLimitExtension

Maximum number of credits that the credit limit can be exceeded by. Managed by the workspace admin. `"unlimited"` means no cap, `0` means usage-based billing is disabled.


## Supported Types

### 

```go
subscriptionResponseModelMaxCreditLimitExtension := components.CreateSubscriptionResponseModelMaxCreditLimitExtensionInteger(int64{/* values here */})
```

### 

```go
subscriptionResponseModelMaxCreditLimitExtension := components.CreateSubscriptionResponseModelMaxCreditLimitExtensionStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch subscriptionResponseModelMaxCreditLimitExtension.Type {
	case components.SubscriptionResponseModelMaxCreditLimitExtensionTypeInteger:
		// subscriptionResponseModelMaxCreditLimitExtension.Integer is populated
	case components.SubscriptionResponseModelMaxCreditLimitExtensionTypeStr:
		// subscriptionResponseModelMaxCreditLimitExtension.Str is populated
}
```
