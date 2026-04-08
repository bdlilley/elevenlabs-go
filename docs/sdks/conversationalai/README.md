# ConversationalAI

## Overview

### Available Operations

* [CreateFolderRoute](#createfolderroute) - Create Folder
* [PostKnowledgeBaseMoveRoute](#postknowledgebasemoveroute) - Move Entity To Folder
* [PostKnowledgeBaseBulkMoveRoute](#postknowledgebasebulkmoveroute) - Bulk Move Entities To Folder

## CreateFolderRoute

Create a folder used for grouping documents together.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_folder_route" method="post" path="/v1/convai/knowledge-base/folder" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.ConversationalAI.CreateFolderRoute(ctx, components.BodyCreateFolderV1ConvaiKnowledgeBaseFolderPost{
        Name: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AddKnowledgeBaseResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyCreateFolderV1ConvaiKnowledgeBaseFolderPost](../../models/components/bodycreatefolderv1convaiknowledgebasefolderpost.md)                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateFolderRouteResponse](../../models/operations/createfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PostKnowledgeBaseMoveRoute

Moves the entity from one folder to another.

### Example Usage

<!-- UsageSnippet language="go" operationID="post_knowledge_base_move_route" method="post" path="/v1/convai/knowledge-base/{document_id}/move" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.ConversationalAI.PostKnowledgeBaseMoveRoute(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                             | Type                                                                                                                                                                  | Required                                                                                                                                                              | Description                                                                                                                                                           | Example                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                 | :heavy_check_mark:                                                                                                                                                    | The context to use for the request.                                                                                                                                   |                                                                                                                                                                       |
| `documentID`                                                                                                                                                          | `string`                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | The id of a document from the knowledge base. This is returned on document addition.                                                                                  | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                            | optionalnullable.OptionalNullable[`string`]                                                                                                                           | :heavy_minus_sign:                                                                                                                                                    | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.             |                                                                                                                                                                       |
| `body`                                                                                                                                                                | [*components.BodyMoveEntityToFolderV1ConvaiKnowledgeBaseDocumentIDMovePost](../../models/components/bodymoveentitytofolderv1convaiknowledgebasedocumentidmovepost.md) | :heavy_minus_sign:                                                                                                                                                    | N/A                                                                                                                                                                   |                                                                                                                                                                       |
| `opts`                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                              | :heavy_minus_sign:                                                                                                                                                    | The options for this request.                                                                                                                                         |                                                                                                                                                                       |

### Response

**[*operations.PostKnowledgeBaseMoveRouteResponse](../../models/operations/postknowledgebasemoverouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PostKnowledgeBaseBulkMoveRoute

Moves multiple entities from one folder to another.

### Example Usage

<!-- UsageSnippet language="go" operationID="post_knowledge_base_bulk_move_route" method="post" path="/v1/convai/knowledge-base/bulk-move" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.ConversationalAI.PostKnowledgeBaseBulkMoveRoute(ctx, components.BodyBulkMoveEntitiesToFolderV1ConvaiKnowledgeBaseBulkMovePost{
        DocumentIds: []string{
            "21m00Tcm4TlvDq8ikWAM",
            "31m00Tcm4TlvDq8ikWBM",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                            | Type                                                                                                                                                                 | Required                                                                                                                                                             | Description                                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                | :heavy_check_mark:                                                                                                                                                   | The context to use for the request.                                                                                                                                  |
| `body`                                                                                                                                                               | [components.BodyBulkMoveEntitiesToFolderV1ConvaiKnowledgeBaseBulkMovePost](../../models/components/bodybulkmoveentitiestofolderv1convaiknowledgebasebulkmovepost.md) | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                           | optionalnullable.OptionalNullable[`string`]                                                                                                                          | :heavy_minus_sign:                                                                                                                                                   | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.            |
| `opts`                                                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                                                             | :heavy_minus_sign:                                                                                                                                                   | The options for this request.                                                                                                                                        |

### Response

**[*operations.PostKnowledgeBaseBulkMoveRouteResponse](../../models/operations/postknowledgebasebulkmoverouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |