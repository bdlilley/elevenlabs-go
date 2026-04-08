# BodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissions

The permissions of the XI API.


## Supported Types

### 

```go
bodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissions := components.CreateBodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissionsArrayOfPermissionType([]components.PermissionType{/* values here */})
```

### 

```go
bodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissions := components.CreateBodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissionsStr(string{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch bodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissions.Type {
	case components.BodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissionsTypeArrayOfPermissionType:
		// bodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissions.ArrayOfPermissionType is populated
	case components.BodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissionsTypeStr:
		// bodyEditServiceAccountAPIKeyV1ServiceAccountsServiceAccountUserIDAPIKeysAPIKeyIDPatchPermissions.Str is populated
}
```
