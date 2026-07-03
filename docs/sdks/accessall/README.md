# AccessAll

## Overview

Endpoints accessible to all authenticated callers regardless of scope.

### Available Operations

* [UsageByProductOverTime](#usagebyproductovertime) - Get Workspace Usage
* [RequestsList](#requestslist) - List Api Requests

## UsageByProductOverTime

Returns credit usage broken down by product type over time. The response is a tabular structure with columns, column_types, column_units, and rows.

### Example Usage

<!-- UsageSnippet language="go" operationID="usage_by_product_over_time" method="post" path="/v1/workspace/analytics/query/usage-by-product-over-time" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AccessAll.UsageByProductOverTime(ctx, components.BodyGetWorkspaceUsageV1WorkspaceAnalyticsQueryUsageByProductOverTimePost{
        StartTime: 918816,
        EndTime: 838021,
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceAnalyticsQueryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                  | Type                                                                                                                                                                                       | Required                                                                                                                                                                                   | Description                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                         | The context to use for the request.                                                                                                                                                        |
| `request`                                                                                                                                                                                  | [components.BodyGetWorkspaceUsageV1WorkspaceAnalyticsQueryUsageByProductOverTimePost](../../models/components/bodygetworkspaceusagev1workspaceanalyticsqueryusagebyproductovertimepost.md) | :heavy_check_mark:                                                                                                                                                                         | The request object to use for the request.                                                                                                                                                 |
| `opts`                                                                                                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                                         | The options for this request.                                                                                                                                                              |

### Response

**[*operations.UsageByProductOverTimeResponse](../../models/operations/usagebyproductovertimeresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RequestsList

Returns a list of API requests. Supports filtering by time range, column filters, and search terms. At least one of start_time or end_time must be provided. An optional sort parameter controls timestamp ordering. Results are ordered by timestamp. Descending if end_time is used, ascending if start_time is used. The response is a tabular structure with columns, column_types, column_units, and rows.

### Example Usage

<!-- UsageSnippet language="go" operationID="requests_list" method="post" path="/v1/workspace/analytics/requests" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AccessAll.RequestsList(ctx, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceAnalyticsQueryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                        | Type                                                                                                                                             | Required                                                                                                                                         | Description                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                            | :heavy_check_mark:                                                                                                                               | The context to use for the request.                                                                                                              |
| `request`                                                                                                                                        | [components.BodyListAPIRequestsV1WorkspaceAnalyticsRequestsPost](../../models/components/bodylistapirequestsv1workspaceanalyticsrequestspost.md) | :heavy_check_mark:                                                                                                                               | The request object to use for the request.                                                                                                       |
| `opts`                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                         | :heavy_minus_sign:                                                                                                                               | The options for this request.                                                                                                                    |

### Response

**[*operations.RequestsListResponse](../../models/operations/requestslistresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |