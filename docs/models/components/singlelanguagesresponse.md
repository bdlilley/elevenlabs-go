# SingleLanguagesResponse


## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `Kind`                                                                               | `*string`                                                                            | :heavy_minus_sign:                                                                   | Indicates this response contains single languages (not source-to-destination pairs). |
| `Languages`                                                                          | [][components.LanguageInfo](../../models/components/languageinfo.md)                 | :heavy_check_mark:                                                                   | The list of available languages.                                                     |