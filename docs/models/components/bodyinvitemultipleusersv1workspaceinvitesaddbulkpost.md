# BodyInviteMultipleUsersV1WorkspaceInvitesAddBulkPost


## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 | Example                                                     |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `Emails`                                                    | []`string`                                                  | :heavy_check_mark:                                          | The email of the customer                                   | john.doe@testmail.com                                       |
| `SeatType`                                                  | [*components.SeatType](../../models/components/seattype.md) | :heavy_minus_sign:                                          | The seat type of the user                                   |                                                             |
| `GroupIds`                                                  | []`string`                                                  | :heavy_minus_sign:                                          | The group ids of the user                                   | [<br/>"group_id_1",<br/>"group_id_2"<br/>]                  |