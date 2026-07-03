# DeleteCalendarEventParams

Permanently remove a previously-cancelled calendar event.

This delete tool is the irreversible follow-up to cancel_calendar_event.
The backend rejects the call (422) if the event hasn't been
cancelled yet, so the only safe path is cancel-then-delete.


## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `SmbToolType`      | `*string`          | :heavy_minus_sign: | N/A                |