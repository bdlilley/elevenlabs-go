# TestRunResultBucket


## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `TestRunIds`                                                         | []`string`                                                           | :heavy_check_mark:                                                   | N/A                                                                  |
| `Title`                                                              | `string`                                                             | :heavy_check_mark:                                                   | Short one-line title for this bucket                                 |
| `Reason`                                                             | `string`                                                             | :heavy_check_mark:                                                   | Short summary of why the test runs in this bucket passed or failed   |
| `Status`                                                             | [components.TestRunStatus](../../models/components/testrunstatus.md) | :heavy_check_mark:                                                   | N/A                                                                  |