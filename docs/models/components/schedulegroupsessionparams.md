# ScheduleGroupSessionParams

Schedule a single instance of a group service.

The session's duration is derived from the parent service so the assistant
only has to pin start time, the (optional) instructor / room, and the
location. Participants register separately via
``register_for_group_session``.


## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `SmbToolType`      | `*string`          | :heavy_minus_sign: | N/A                |