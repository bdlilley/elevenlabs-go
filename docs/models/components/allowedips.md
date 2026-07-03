# AllowedIps

List of IP addresses or CIDR ranges allowed to use this API key. Each entry may be a CIDR range (e.g. '10.0.0.0/24') or a bare IP address (normalized to /32 or /128). On create, omit or pass null to allow all IPs. On update, omit to leave the allowlist unchanged, or pass "clear" to remove it.


## Supported Types

### 

```go
allowedIps := components.CreateAllowedIpsArrayOfStr([]string{/* values here */})
```

### AllowedIpsEnum

```go
allowedIps := components.CreateAllowedIpsAllowedIpsEnum(components.AllowedIpsEnum{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch allowedIps.Type {
	case components.AllowedIpsTypeArrayOfStr:
		// allowedIps.ArrayOfStr is populated
	case components.AllowedIpsTypeAllowedIpsEnum:
		// allowedIps.AllowedIpsEnum is populated
}
```
