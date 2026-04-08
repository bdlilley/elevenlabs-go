# PronunciationDictionary

## Overview

### Available Operations

* [AddFromFile](#addfromfile) - Add A Pronunciation Dictionary
* [AddFromRules](#addfromrules) - Add A Pronunciation Dictionary
* [GetPronunciationDictionaryMetadata](#getpronunciationdictionarymetadata) - Get Metadata For A Pronunciation Dictionary
* [PatchPronunciationDictionary](#patchpronunciationdictionary) - Update Pronunciation Dictionary
* [SetRules](#setrules) - Set Rules On The Pronunciation Dictionary
* [AddRules](#addrules) - Add Rules To The Pronunciation Dictionary
* [RemoveRules](#removerules) - Remove Rules From The Pronunciation Dictionary
* [GetPronunciationDictionaryVersionPls](#getpronunciationdictionaryversionpls) - Get A Pls File With A Pronunciation Dictionary Version Rules
* [GetPronunciationDictionariesMetadata](#getpronunciationdictionariesmetadata) - Get Pronunciation Dictionaries

## AddFromFile

Creates a new pronunciation dictionary from a lexicon .PLS file

### Example Usage

<!-- UsageSnippet language="go" operationID="add_from_file" method="post" path="/v1/pronunciation-dictionaries/add-from-file" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.PronunciationDictionary.AddFromFile(ctx, components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromFilePost{
        Name: "My Dictionary",
        Description: optionalnullable.From(elevenlabsgo.Pointer("Contains pronunciation's of our character names")),
        WorkspaceAccess: optionalnullable.From(elevenlabsgo.Pointer(components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromFilePostWorkspaceAccessViewer)),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AddPronunciationDictionaryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                    | Type                                                                                                                                                                                         | Required                                                                                                                                                                                     | Description                                                                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                           | The context to use for the request.                                                                                                                                                          |
| `body`                                                                                                                                                                                       | [components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromFilePost](../../models/components/bodyaddapronunciationdictionaryv1pronunciationdictionariesaddfromfilepost.md) | :heavy_check_mark:                                                                                                                                                                           | N/A                                                                                                                                                                                          |
| `xiAPIKey`                                                                                                                                                                                   | optionalnullable.OptionalNullable[`string`]                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                           | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                    |
| `opts`                                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                           | The options for this request.                                                                                                                                                                |

### Response

**[*operations.AddFromFileResponse](../../models/operations/addfromfileresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddFromRules

Creates a new pronunciation dictionary from provided rules.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_from_rules" method="post" path="/v1/pronunciation-dictionaries/add-from-rules" -->
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
    )

    res, err := s.PronunciationDictionary.AddFromRules(ctx, components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromRulesPost{
        Rules: []components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromRulesPostRule{
            components.CreateBodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromRulesPostRulePhoneme(
                components.PronunciationDictionaryPhonemeRuleRequestModel{
                    StringToReplace: "<value>",
                    Phoneme: "<value>",
                    Alphabet: "<value>",
                },
            ),
        },
        Name: "My Dictionary",
        Description: optionalnullable.From(elevenlabsgo.Pointer("Contains pronunciation's of our character names")),
        WorkspaceAccess: optionalnullable.From(elevenlabsgo.Pointer(components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromRulesPostWorkspaceAccessViewer)),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AddPronunciationDictionaryResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                      | Type                                                                                                                                                                                           | Required                                                                                                                                                                                       | Description                                                                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                          | :heavy_check_mark:                                                                                                                                                                             | The context to use for the request.                                                                                                                                                            |
| `body`                                                                                                                                                                                         | [components.BodyAddAPronunciationDictionaryV1PronunciationDictionariesAddFromRulesPost](../../models/components/bodyaddapronunciationdictionaryv1pronunciationdictionariesaddfromrulespost.md) | :heavy_check_mark:                                                                                                                                                                             | N/A                                                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                                                     | optionalnullable.OptionalNullable[`string`]                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                                                             | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                      |
| `opts`                                                                                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                                             | The options for this request.                                                                                                                                                                  |

### Response

**[*operations.AddFromRulesResponse](../../models/operations/addfromrulesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPronunciationDictionaryMetadata

Get metadata for a pronunciation dictionary

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pronunciation_dictionary_metadata" method="get" path="/v1/pronunciation-dictionaries/{pronunciation_dictionary_id}" -->
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
    )

    res, err := s.PronunciationDictionary.GetPronunciationDictionaryMetadata(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetPronunciationDictionaryWithRulesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `pronunciationDictionaryID`                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of the pronunciation dictionary                                                                                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetPronunciationDictionaryMetadataResponse](../../models/operations/getpronunciationdictionarymetadataresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PatchPronunciationDictionary

Partially update the pronunciation dictionary without changing the version

### Example Usage

<!-- UsageSnippet language="go" operationID="patch_pronunciation_dictionary" method="patch" path="/v1/pronunciation-dictionaries/{pronunciation_dictionary_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.PronunciationDictionary.PatchPronunciationDictionary(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil), &components.BodyUpdatePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDPatch{
        Archived: elevenlabsgo.Pointer(true),
        Name: elevenlabsgo.Pointer("My Dictionary"),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetPronunciationDictionaryMetadataResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                       | Type                                                                                                                                                                                                                            | Required                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                     | Example                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                           | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                                                                              | The context to use for the request.                                                                                                                                                                                             |                                                                                                                                                                                                                                 |
| `pronunciationDictionaryID`                                                                                                                                                                                                     | `string`                                                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                                                              | The id of the pronunciation dictionary                                                                                                                                                                                          | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                                                                                      | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                                                              | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                       |                                                                                                                                                                                                                                 |
| `body`                                                                                                                                                                                                                          | [*components.BodyUpdatePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDPatch](../../models/components/bodyupdatepronunciationdictionaryv1pronunciationdictionariespronunciationdictionaryidpatch.md) | :heavy_minus_sign:                                                                                                                                                                                                              | N/A                                                                                                                                                                                                                             |                                                                                                                                                                                                                                 |
| `opts`                                                                                                                                                                                                                          | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                        | :heavy_minus_sign:                                                                                                                                                                                                              | The options for this request.                                                                                                                                                                                                   |                                                                                                                                                                                                                                 |

### Response

**[*operations.PatchPronunciationDictionaryResponse](../../models/operations/patchpronunciationdictionaryresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SetRules

Replaces all existing rules on the pronunciation dictionary with the provided ones.

### Example Usage

<!-- UsageSnippet language="go" operationID="set_rules" method="post" path="/v1/pronunciation-dictionaries/{pronunciation_dictionary_id}/set-rules" -->
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
    )

    res, err := s.PronunciationDictionary.SetRules(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodySetRulesOnThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDSetRulesPost{
        Rules: []components.BodySetRulesOnThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDSetRulesPostRule{
            components.CreateBodySetRulesOnThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDSetRulesPostRulePhoneme(
                components.PronunciationDictionaryPhonemeRuleRequestModel{
                    StringToReplace: "<value>",
                    Phoneme: "<value>",
                    Alphabet: "<value>",
                },
            ),
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.PronunciationDictionaryRulesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                  | Type                                                                                                                                                                                                                                                       | Required                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                | Example                                                                                                                                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                                                         | The context to use for the request.                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                            |
| `pronunciationDictionaryID`                                                                                                                                                                                                                                | `string`                                                                                                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                                                                                                         | The id of the pronunciation dictionary                                                                                                                                                                                                                     | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                     | [components.BodySetRulesOnThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDSetRulesPost](../../models/components/bodysetrulesonthepronunciationdictionaryv1pronunciationdictionariespronunciationdictionaryidsetrulespost.md) | :heavy_check_mark:                                                                                                                                                                                                                                         | N/A                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                                                                                                                 | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                | :heavy_minus_sign:                                                                                                                                                                                                                                         | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                  |                                                                                                                                                                                                                                                            |
| `opts`                                                                                                                                                                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                                                                                                         | The options for this request.                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                            |

### Response

**[*operations.SetRulesResponse](../../models/operations/setrulesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddRules

Add rules to the pronunciation dictionary. If a rule with the same string_to_replace already exists, it will be replaced.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_rules" method="post" path="/v1/pronunciation-dictionaries/{pronunciation_dictionary_id}/add-rules" -->
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
    )

    res, err := s.PronunciationDictionary.AddRules(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyAddRulesToThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDAddRulesPost{
        Rules: []components.BodyAddRulesToThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDAddRulesPostRule{
            components.CreateBodyAddRulesToThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDAddRulesPostRuleAlias(
                components.PronunciationDictionaryAliasRuleRequestModel{
                    StringToReplace: "<value>",
                    Alias: "<value>",
                },
            ),
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.PronunciationDictionaryRulesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                  | Type                                                                                                                                                                                                                                                       | Required                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                | Example                                                                                                                                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                                                         | The context to use for the request.                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                            |
| `pronunciationDictionaryID`                                                                                                                                                                                                                                | `string`                                                                                                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                                                                                                         | The id of the pronunciation dictionary                                                                                                                                                                                                                     | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                     | [components.BodyAddRulesToThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDAddRulesPost](../../models/components/bodyaddrulestothepronunciationdictionaryv1pronunciationdictionariespronunciationdictionaryidaddrulespost.md) | :heavy_check_mark:                                                                                                                                                                                                                                         | N/A                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                                                                                                                 | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                | :heavy_minus_sign:                                                                                                                                                                                                                                         | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                  |                                                                                                                                                                                                                                                            |
| `opts`                                                                                                                                                                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                                                                                                         | The options for this request.                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                            |

### Response

**[*operations.AddRulesResponse](../../models/operations/addrulesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RemoveRules

Remove rules from the pronunciation dictionary

### Example Usage

<!-- UsageSnippet language="go" operationID="remove_rules" method="post" path="/v1/pronunciation-dictionaries/{pronunciation_dictionary_id}/remove-rules" -->
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
    )

    res, err := s.PronunciationDictionary.RemoveRules(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyRemoveRulesFromThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDRemoveRulesPost{
        RuleStrings: []string{
            "['a', 'b']",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.PronunciationDictionaryRulesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                                                                  | Type                                                                                                                                                                                                                                                                       | Required                                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                | Example                                                                                                                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                                                                         | The context to use for the request.                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                            |
| `pronunciationDictionaryID`                                                                                                                                                                                                                                                | `string`                                                                                                                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                                                                                                                         | The id of the pronunciation dictionary                                                                                                                                                                                                                                     | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                                                       |
| `body`                                                                                                                                                                                                                                                                     | [components.BodyRemoveRulesFromThePronunciationDictionaryV1PronunciationDictionariesPronunciationDictionaryIDRemoveRulesPost](../../models/components/bodyremoverulesfromthepronunciationdictionaryv1pronunciationdictionariespronunciationdictionaryidremoverulespost.md) | :heavy_check_mark:                                                                                                                                                                                                                                                         | N/A                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                                                                                                                                 | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                                                                | :heavy_minus_sign:                                                                                                                                                                                                                                                         | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                                                                  |                                                                                                                                                                                                                                                                            |
| `opts`                                                                                                                                                                                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                                                                                                                         | The options for this request.                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                            |

### Response

**[*operations.RemoveRulesResponse](../../models/operations/removerulesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPronunciationDictionaryVersionPls

Get a PLS file with a pronunciation dictionary version rules

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pronunciation_dictionary_version_pls" method="get" path="/v1/pronunciation-dictionaries/{dictionary_id}/{version_id}/download" -->
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
    )

    res, err := s.PronunciationDictionary.GetPronunciationDictionaryVersionPls(ctx, "21m00Tcm4TlvDq8ikWAM", "BdF0s0aZ3oFoKnDYdTox", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseStream != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `dictionaryID`                                                                                                                                            | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of the pronunciation dictionary                                                                                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `versionID`                                                                                                                                               | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of the pronunciation dictionary version                                                                                                            | BdF0s0aZ3oFoKnDYdTox                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetPronunciationDictionaryVersionPlsResponse](../../models/operations/getpronunciationdictionaryversionplsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPronunciationDictionariesMetadata

Get a list of the pronunciation dictionaries you have access to and their metadata

### Example Usage

<!-- UsageSnippet language="go" operationID="get_pronunciation_dictionaries_metadata" method="get" path="/v1/pronunciation-dictionaries" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.PronunciationDictionary.GetPronunciationDictionariesMetadata(ctx, operations.GetPronunciationDictionariesMetadataRequest{
        Sort: optionalnullable.From(elevenlabsgo.Pointer(operations.SortCreationTimeUnix)),
        SortDirection: optionalnullable.From(elevenlabsgo.Pointer("descending")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetPronunciationDictionariesMetadataResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                        | Type                                                                                                                             | Required                                                                                                                         | Description                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                            | :heavy_check_mark:                                                                                                               | The context to use for the request.                                                                                              |
| `request`                                                                                                                        | [operations.GetPronunciationDictionariesMetadataRequest](../../models/operations/getpronunciationdictionariesmetadatarequest.md) | :heavy_check_mark:                                                                                                               | The request object to use for the request.                                                                                       |
| `opts`                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                         | :heavy_minus_sign:                                                                                                               | The options for this request.                                                                                                    |

### Response

**[*operations.GetPronunciationDictionariesMetadataResponse](../../models/operations/getpronunciationdictionariesmetadataresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |