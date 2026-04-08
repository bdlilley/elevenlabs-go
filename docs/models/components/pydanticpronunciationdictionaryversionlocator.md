# PydanticPronunciationDictionaryVersionLocator

A locator for other documents to be able to reference a specific dictionary and it's version.
This is a pydantic version of PronunciationDictionaryVersionLocatorDBModel.
Required to ensure compat with the rest of the agent data models.


## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `PronunciationDictionaryID`                           | `string`                                              | :heavy_check_mark:                                    | The ID of the pronunciation dictionary                |
| `VersionID`                                           | `*string`                                             | :heavy_check_mark:                                    | The ID of the version of the pronunciation dictionary |