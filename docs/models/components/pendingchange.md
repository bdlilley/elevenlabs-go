# PendingChange

The pending change for the user.


## Supported Types

### PendingSubscriptionSwitchResponseModel

```go
pendingChange := components.CreatePendingChangePendingSubscriptionSwitchResponseModel(components.PendingSubscriptionSwitchResponseModel{/* values here */})
```

### PendingCancellationResponseModel

```go
pendingChange := components.CreatePendingChangePendingCancellationResponseModel(components.PendingCancellationResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch pendingChange.Type {
	case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
		// pendingChange.PendingSubscriptionSwitchResponseModel is populated
	case components.PendingChangeTypePendingCancellationResponseModel:
		// pendingChange.PendingCancellationResponseModel is populated
}
```
