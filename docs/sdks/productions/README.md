# Productions

## Overview

Access and manage ElevenProductions orders.

### Available Operations

* [PublicListOrders](#publiclistorders) - List Orders
* [PublicCreateOrder](#publiccreateorder) - Create Order
* [PublicGetOrder](#publicgetorder) - Get Order
* [PublicUpdateOrder](#publicupdateorder) - Update Order
* [PublicRegisterMedia](#publicregistermedia) - Register Media
* [PublicGetMediaInfo](#publicgetmediainfo) - Get Media Info
* [PublicUpsertOrderItem](#publicupsertorderitem) - Upsert Order Item
* [PublicRemoveOrderItem](#publicremoveorderitem) - Remove Order Item
* [PublicSubmitOrder](#publicsubmitorder) - Submit Order
* [PublicGetOrderDeliverables](#publicgetorderdeliverables) - Get Order Deliverables
* [PublicGetAvailableLanguages](#publicgetavailablelanguages) - Get Available Languages

## PublicListOrders

Lists Productions orders in the workspace. Supports filtering by status and date range, with pagination.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_list_orders" method="get" path="/v1/productions/orders" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.Productions.PublicListOrders(ctx, operations.PublicListOrdersRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.ListOrdersResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `ctx`                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                    | :heavy_check_mark:                                                                       | The context to use for the request.                                                      |
| `request`                                                                                | [operations.PublicListOrdersRequest](../../models/operations/publiclistordersrequest.md) | :heavy_check_mark:                                                                       | The request object to use for the request.                                               |
| `opts`                                                                                   | [][operations.Option](../../models/operations/option.md)                                 | :heavy_minus_sign:                                                                       | The options for this request.                                                            |

### Response

**[*operations.PublicListOrdersResponse](../../models/operations/publiclistordersresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicCreateOrder

Creates a new Productions order in the workspace. The order starts in the open state and can be configured with items before submission.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_create_order" method="post" path="/v1/productions/orders" -->
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

    res, err := s.Productions.PublicCreateOrder(ctx, &components.CreateOrderRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateOrderResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `ctx`                                                                          | [context.Context](https://pkg.go.dev/context#Context)                          | :heavy_check_mark:                                                             | The context to use for the request.                                            |
| `request`                                                                      | [components.CreateOrderRequest](../../models/components/createorderrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |
| `opts`                                                                         | [][operations.Option](../../models/operations/option.md)                       | :heavy_minus_sign:                                                             | The options for this request.                                                  |

### Response

**[*operations.PublicCreateOrderResponse](../../models/operations/publiccreateorderresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicGetOrder

Retrieves full details for a Productions order.

Quote and pricing information may not be available immediately; if you wish to see the quote before submission, you may need to poll the order details until it is ready.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_get_order" method="get" path="/v1/productions/orders/{order_id}" -->
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

    res, err := s.Productions.PublicGetOrder(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.OrderResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `orderID`                                                | `string`                                                 | :heavy_check_mark:                                       | The ID of the order.                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.PublicGetOrderResponse](../../models/operations/publicgetorderresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicUpdateOrder

Updates an open order.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_update_order" method="patch" path="/v1/productions/orders/{order_id}" -->
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

    res, err := s.Productions.PublicUpdateOrder(ctx, "<id>", components.BodyUpdateOrderV1ProductionsOrdersOrderIDPatch{
        Request: components.UpdateOrderRequest{
            Name: "Spanish Dubs",
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.UpdateOrderResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                              | Type                                                                                                                                   | Required                                                                                                                               | Description                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                  | :heavy_check_mark:                                                                                                                     | The context to use for the request.                                                                                                    |
| `orderID`                                                                                                                              | `string`                                                                                                                               | :heavy_check_mark:                                                                                                                     | The ID of the order.                                                                                                                   |
| `body`                                                                                                                                 | [components.BodyUpdateOrderV1ProductionsOrdersOrderIDPatch](../../models/components/bodyupdateorderv1productionsordersorderidpatch.md) | :heavy_check_mark:                                                                                                                     | N/A                                                                                                                                    |
| `opts`                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                               | :heavy_minus_sign:                                                                                                                     | The options for this request.                                                                                                          |

### Response

**[*operations.PublicUpdateOrderResponse](../../models/operations/publicupdateorderresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicRegisterMedia

Registers a media file with an order, either by uploading it directly or by providing a URL to fetch it from. Exactly one of `media` or `media_url` must be provided. The registered media can then be referenced when adding order items.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_register_media" method="post" path="/v1/productions/orders/{order_id}/media" -->
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

    res, err := s.Productions.PublicRegisterMedia(ctx, "<id>", components.BodyRegisterMediaV1ProductionsOrdersOrderIDMediaPost{
        DeclaredLanguage: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.RegisterMediaResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                          | Type                                                                                                                                               | Required                                                                                                                                           | Description                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                                                              | :heavy_check_mark:                                                                                                                                 | The context to use for the request.                                                                                                                |
| `orderID`                                                                                                                                          | `string`                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | The ID of the order to which this media will be attached.                                                                                          |
| `body`                                                                                                                                             | [components.BodyRegisterMediaV1ProductionsOrdersOrderIDMediaPost](../../models/components/bodyregistermediav1productionsordersorderidmediapost.md) | :heavy_check_mark:                                                                                                                                 | N/A                                                                                                                                                |
| `opts`                                                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                                                           | :heavy_minus_sign:                                                                                                                                 | The options for this request.                                                                                                                      |

### Response

**[*operations.PublicRegisterMediaResponse](../../models/operations/publicregistermediaresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicGetMediaInfo

Retrieves metadata and a time-limited download URL for a previously uploaded media file.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_get_media_info" method="get" path="/v1/productions/orders/{order_id}/media/{media_id}" -->
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

    res, err := s.Productions.PublicGetMediaInfo(ctx, "<id>", "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.OrderMediaResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `orderID`                                                | `string`                                                 | :heavy_check_mark:                                       | The ID of the order.                                     |
| `mediaID`                                                | `string`                                                 | :heavy_check_mark:                                       | The ID of the media file.                                |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.PublicGetMediaInfoResponse](../../models/operations/publicgetmediainforesponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicUpsertOrderItem

Adds or updates an order item on an open order. Returns the item ID and the quoted price.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_upsert_order_item" method="post" path="/v1/productions/orders/{order_id}/items" -->
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

    res, err := s.Productions.PublicUpsertOrderItem(ctx, "<id>", components.BodyUpsertOrderItemV1ProductionsOrdersOrderIDItemsPost{
        Request: components.UpsertOrderItemRequest{
            Item: components.CreateOrderItemRequestInputDub(
                components.DubOrderItemRequest{
                    MediaID: "prodmedia_01jgatk6h0fwxrtbjade61yqhx",
                    SourceLanguage: "en",
                    DestinationLanguages: []string{
                        "hi",
                        "fr-FR",
                        "de",
                    },
                    IncludeCaptions: true,
                    IncludeSourceCaptions: false,
                    Instructions: elevenlabsgo.Pointer("Voices don't need to match the originals, prioritize native-sounding voices"),
                    CaptionsSdh: elevenlabsgo.Pointer(false),
                },
            ),
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.UpsertOrderItemResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                              | Type                                                                                                                                                   | Required                                                                                                                                               | Description                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                                  | :heavy_check_mark:                                                                                                                                     | The context to use for the request.                                                                                                                    |
| `orderID`                                                                                                                                              | `string`                                                                                                                                               | :heavy_check_mark:                                                                                                                                     | The ID of the order.                                                                                                                                   |
| `body`                                                                                                                                                 | [components.BodyUpsertOrderItemV1ProductionsOrdersOrderIDItemsPost](../../models/components/bodyupsertorderitemv1productionsordersorderiditemspost.md) | :heavy_check_mark:                                                                                                                                     | N/A                                                                                                                                                    |
| `opts`                                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                                               | :heavy_minus_sign:                                                                                                                                     | The options for this request.                                                                                                                          |

### Response

**[*operations.PublicUpsertOrderItemResponse](../../models/operations/publicupsertorderitemresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicRemoveOrderItem

Removes an order item from an open order.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_remove_order_item" method="delete" path="/v1/productions/orders/{order_id}/items/{item_id}" -->
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

    res, err := s.Productions.PublicRemoveOrderItem(ctx, "<id>", "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.RemoveOrderItemResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `orderID`                                                | `string`                                                 | :heavy_check_mark:                                       | The ID of the order.                                     |
| `itemID`                                                 | `string`                                                 | :heavy_check_mark:                                       | The ID of the order item.                                |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.PublicRemoveOrderItemResponse](../../models/operations/publicremoveorderitemresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicSubmitOrder

Submits an open order for processing. The order must have at least one item. Once submitted, items can no longer be modified.

Upon submission, the workspace will be charged for the order. The quote is based on information extracted from the uploaded media, such as its duration. The quote may not be available immediately; if you wish to see the quote before submission, you may need to poll the order details until the quote is ready.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_submit_order" method="post" path="/v1/productions/orders/{order_id}/submit" -->
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

    res, err := s.Productions.PublicSubmitOrder(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.SubmitOrderResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `orderID`                                                | `string`                                                 | :heavy_check_mark:                                       | The ID of the order.                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.PublicSubmitOrderResponse](../../models/operations/publicsubmitorderresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicGetOrderDeliverables

Retrieves the delivered files for a completed order. Returns an empty list if the order is not yet completed.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_get_order_deliverables" method="get" path="/v1/productions/orders/{order_id}/deliverables" -->
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

    res, err := s.Productions.PublicGetOrderDeliverables(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.OrderDeliverablesResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `orderID`                                                | `string`                                                 | :heavy_check_mark:                                       | The ID of the order.                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.PublicGetOrderDeliverablesResponse](../../models/operations/publicgetorderdeliverablesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PublicGetAvailableLanguages

Returns the available languages for a given order item kind.

### Example Usage

<!-- UsageSnippet language="go" operationID="public_get_available_languages" method="get" path="/v1/productions/orders/languages/{order_item_kind}" -->
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

    res, err := s.Productions.PublicGetAvailableLanguages(ctx, components.OrderItemKindSubtitles)
    if err != nil {
        log.Fatal(err)
    }
    if res.LanguagesResponse != nil {
        switch res.LanguagesResponse.Type {
            case components.LanguagesResponseTypePair:
                // res.LanguagesResponse.PairedLanguagesResponse is populated
            case components.LanguagesResponseTypeSingle:
                // res.LanguagesResponse.SingleLanguagesResponse is populated
        }

    }
}
```

### Parameters

| Parameter                                                            | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `ctx`                                                                | [context.Context](https://pkg.go.dev/context#Context)                | :heavy_check_mark:                                                   | The context to use for the request.                                  |
| `orderItemKind`                                                      | [components.OrderItemKind](../../models/components/orderitemkind.md) | :heavy_check_mark:                                                   | The kind of order item.                                              |
| `opts`                                                               | [][operations.Option](../../models/operations/option.md)             | :heavy_minus_sign:                                                   | The options for this request.                                        |

### Response

**[*operations.PublicGetAvailableLanguagesResponse](../../models/operations/publicgetavailablelanguagesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |