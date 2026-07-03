# PairedLanguagesResponse


## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `Kind`                                                                       | `*string`                                                                    | :heavy_minus_sign:                                                           | Indicates this response contains source-to-destination language pairs.       |
| `LanguagePairs`                                                              | [][components.LanguagePairInfo](../../models/components/languagepairinfo.md) | :heavy_check_mark:                                                           | The list of available source-to-destination language mappings.               |