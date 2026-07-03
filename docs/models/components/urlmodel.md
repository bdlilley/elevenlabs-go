# URLModel

OCSF URL object.

Spec: https://schema.ocsf.io/1.6.0/objects/url


## Fields

| Field                    | Type                     | Required                 | Description              |
| ------------------------ | ------------------------ | ------------------------ | ------------------------ |
| `URLString`              | `*string`                | :heavy_minus_sign:       | Full URL string          |
| `Scheme`                 | `*string`                | :heavy_minus_sign:       | URL scheme (e.g., https) |
| `Hostname`               | `*string`                | :heavy_minus_sign:       | URL hostname             |
| `Port`                   | `*int64`                 | :heavy_minus_sign:       | URL port                 |
| `Path`                   | `*string`                | :heavy_minus_sign:       | URL path                 |
| `QueryString`            | `*string`                | :heavy_minus_sign:       | URL query string         |