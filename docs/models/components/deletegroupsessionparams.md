# DeleteGroupSessionParams

Permanently remove a previously-cancelled group session.

Group analogue of ``delete_calendar_event``: cancel
(``cancel_group_session_for_all``) is the soft, history-preserving step;
this tool is the irreversible follow-up that drops the row from Mongo
and the staff Google Calendar entirely. The backend rejects the call
(422) if the session hasn't been cancelled yet, so the only safe path
is cancel-then-delete.


## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `SmbToolType`      | `*string`          | :heavy_minus_sign: | N/A                |