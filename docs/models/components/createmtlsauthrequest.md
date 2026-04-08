# CreateMTLSAuthRequest

Request model for creating mTLS auth connections.


## Fields

| Field               | Type                | Required            | Description         |
| ------------------- | ------------------- | ------------------- | ------------------- |
| `Name`              | `string`            | :heavy_check_mark:  | N/A                 |
| `AuthType`          | `*string`           | :heavy_minus_sign:  | N/A                 |
| `Provider`          | `string`            | :heavy_check_mark:  | N/A                 |
| `ClientCertificate` | `string`            | :heavy_check_mark:  | N/A                 |
| `ClientKey`         | `string`            | :heavy_check_mark:  | N/A                 |
| `CaCertificate`     | `*string`           | :heavy_minus_sign:  | N/A                 |
| `KeyPassphrase`     | `*string`           | :heavy_minus_sign:  | N/A                 |