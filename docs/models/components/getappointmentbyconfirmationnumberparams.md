# GetAppointmentByConfirmationNumberParams

Look up an appointment by the booking confirmation number the caller quotes.

The confirmation number is the 8-character code shown on the booking
confirmation page (e.g. ``#01ABCDEF``). Callers may read it back with or
without the leading ``#`` and with varied spacing; the tool normalizes
the input and does a prefix match on the stored calendar item id.


## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `SmbToolType`      | `*string`          | :heavy_minus_sign: | N/A                |