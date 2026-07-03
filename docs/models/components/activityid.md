# ActivityID

Activity ID


## Supported Types

### AccountChangeActivityID

```go
activityID := components.CreateActivityIDAccountChangeActivityID(components.AccountChangeActivityID{/* values here */})
```

### AuthenticationActivityID

```go
activityID := components.CreateActivityIDAuthenticationActivityID(components.AuthenticationActivityID{/* values here */})
```

### EntityManagementActivityID

```go
activityID := components.CreateActivityIDEntityManagementActivityID(components.EntityManagementActivityID{/* values here */})
```

### UserAccessManagementActivityID

```go
activityID := components.CreateActivityIDUserAccessManagementActivityID(components.UserAccessManagementActivityID{/* values here */})
```

### GroupManagementActivityID

```go
activityID := components.CreateActivityIDGroupManagementActivityID(components.GroupManagementActivityID{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch activityID.Type {
	case components.ActivityIDTypeAccountChangeActivityID:
		// activityID.AccountChangeActivityID is populated
	case components.ActivityIDTypeAuthenticationActivityID:
		// activityID.AuthenticationActivityID is populated
	case components.ActivityIDTypeEntityManagementActivityID:
		// activityID.EntityManagementActivityID is populated
	case components.ActivityIDTypeUserAccessManagementActivityID:
		// activityID.UserAccessManagementActivityID is populated
	case components.ActivityIDTypeGroupManagementActivityID:
		// activityID.GroupManagementActivityID is populated
}
```
