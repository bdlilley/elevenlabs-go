# BodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissions

The permissions of the XI API.


## Supported Types

### 

```go
bodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissions := components.CreateBodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissionsArrayOfPermissionType([]components.PermissionType{/* values here */})
```

### 

```go
bodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissions := components.CreateBodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissionsStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissions.Type {
	case components.BodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissionsTypeArrayOfPermissionType:
		// bodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissions.ArrayOfPermissionType is populated
	case components.BodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissionsTypeStr:
		// bodyCreateServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysPostPermissions.Str is populated
}
```
