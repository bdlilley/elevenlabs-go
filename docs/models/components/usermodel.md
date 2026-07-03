# UserModel

OCSF User object.

Spec: https://schema.ocsf.io/1.6.0/objects/user


## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `Name`                                                               | `*string`                                                            | :heavy_minus_sign:                                                   | Username                                                             |
| `UID`                                                                | `*string`                                                            | :heavy_minus_sign:                                                   | Unique user identifier                                               |
| `TypeID`                                                             | [*components.UserTypeID](../../models/components/usertypeid.md)      | :heavy_minus_sign:                                                   | OCSF User type IDs.<br/><br/>Spec: https://schema.ocsf.io/1.6.0/objects/user |
| `Type`                                                               | `*string`                                                            | :heavy_minus_sign:                                                   | Account type description                                             |
| `EmailAddr`                                                          | `*string`                                                            | :heavy_minus_sign:                                                   | User email address                                                   |
| `FullName`                                                           | `*string`                                                            | :heavy_minus_sign:                                                   | Full name of the user                                                |
| `Domain`                                                             | `*string`                                                            | :heavy_minus_sign:                                                   | User's domain                                                        |