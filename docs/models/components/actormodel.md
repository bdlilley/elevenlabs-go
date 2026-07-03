# ActorModel

OCSF Actor object - describes the entity that performed the action.

Spec: https://schema.ocsf.io/1.6.0/objects/actor


## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `User`                                                             | [components.UserModel](../../models/components/usermodel.md)       | :heavy_check_mark:                                                 | OCSF User object.<br/><br/>Spec: https://schema.ocsf.io/1.6.0/objects/user |
| `AppName`                                                          | `*string`                                                          | :heavy_minus_sign:                                                 | Client application or service name                                 |
| `AppUID`                                                           | `*string`                                                          | :heavy_minus_sign:                                                 | Client application unique identifier                               |
| `Session`                                                          | map[string]`any`                                                   | :heavy_minus_sign:                                                 | Session information                                                |