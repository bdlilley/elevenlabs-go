# AgentsPlatform

## Overview

### Available Operations

* [GetConversationSignedLink](#getconversationsignedlink) - Get Signed Url
* [~~GetSignedURLDeprecated~~](#getsignedurldeprecated) - Get Signed Url :warning: **Deprecated**
* [GetLivekitToken](#getlivekittoken) - Get Webrtc Token
* [HandleTwilioOutboundCall](#handletwiliooutboundcall) - Handle An Outbound Call Via Twilio
* [RegisterTwilioCall](#registertwiliocall) - Register A Twilio Call And Return Twiml
* [WhatsappOutboundCall](#whatsappoutboundcall) - Make An Outbound Call Via Whatsapp
* [WhatsappOutboundMessage](#whatsappoutboundmessage) - Send An Outbound Message Via Whatsapp
* [CreateAgentRoute](#createagentroute) - Create Agent
* [GetAgentSummariesRoute](#getagentsummariesroute) - Get Agent Summaries
* [GetAgentRoute](#getagentroute) - Get Agent
* [DeleteAgentRoute](#deleteagentroute) - Delete Agent
* [PatchAgentSettingsRoute](#patchagentsettingsroute) - Patches An Agent Settings
* [GetAgentWidgetRoute](#getagentwidgetroute) - Get Agent Widget Config
* [GetAgentLinkRoute](#getagentlinkroute) - Get Shareable Agent Link
* [PostAgentAvatarRoute](#postagentavatarroute) - Post Agent Avatar
* [GetAgentsRoute](#getagentsroute) - List Agents
* [GetAgentKnowledgeBaseSize](#getagentknowledgebasesize) - Returns The Size Of The Agent'S Knowledge Base
* [GetAgentLlmExpectedCostCalculation](#getagentllmexpectedcostcalculation) - Calculate Expected Llm Usage For An Agent
* [DuplicateAgentRoute](#duplicateagentroute) - Duplicate Agent
* [RunConversationSimulationRoute](#runconversationsimulationroute) - Simulates A Conversation
* [RunConversationSimulationRouteStream](#runconversationsimulationroutestream) - Simulates A Conversation (Stream)
* [CreateAgentTestFolderRoute](#createagenttestfolderroute) - Create Agent Test Folder
* [GetAgentTestFolderRoute](#getagenttestfolderroute) - Get Agent Test Folder By Id
* [DeleteAgentTestFolderRoute](#deleteagenttestfolderroute) - Delete Agent Test Folder
* [UpdateAgentTestFolderRoute](#updateagenttestfolderroute) - Update Agent Test Folder
* [AgentTestingBulkMoveRoute](#agenttestingbulkmoveroute) - Bulk Move Tests To Folder
* [GetConversationHistoriesRoute](#getconversationhistoriesroute) - Get Conversations
* [GetConversationUsersRoute](#getconversationusersroute) - Get Conversation Users
* [GetConversationHistoryRoute](#getconversationhistoryroute) - Get Conversation Details
* [DeleteConversationRoute](#deleteconversationroute) - Delete Conversation
* [GetConversationAudioRoute](#getconversationaudioroute) - Get Conversation Audio
* [PostConversationFeedbackRoute](#postconversationfeedbackroute) - Send Conversation Feedback
* [TextSearchConversationMessagesRoute](#textsearchconversationmessagesroute) - Text Search Conversation Messages
* [SmartSearchConversationMessagesRoute](#smartsearchconversationmessagesroute) - Smart Search Conversation Messages
* [ListPhoneNumbersRoute](#listphonenumbersroute) - List Phone Numbers
* [CreatePhoneNumberRoute](#createphonenumberroute) - Import Phone Number
* [GetPhoneNumberRoute](#getphonenumberroute) - Get Phone Number
* [DeletePhoneNumberRoute](#deletephonenumberroute) - Delete Phone Number
* [UpdatePhoneNumberRoute](#updatephonenumberroute) - Update Phone Number
* [GetPublicLlmExpectedCostCalculation](#getpublicllmexpectedcostcalculation) - Calculate Expected Llm Usage
* [ListAvailableLlms](#listavailablellms) - List Available Llms
* [UploadFileRoute](#uploadfileroute) - Upload File
* [CancelFileUploadRoute](#cancelfileuploadroute) - Delete File Upload
* [GetLiveCount](#getlivecount) - Get Live Count
* [GetAgentKnowledgeBaseSummariesRoute](#getagentknowledgebasesummariesroute) - Get Knowledge Base Summaries By Ids
* [GetKnowledgeBaseListRoute](#getknowledgebaselistroute) - Get Knowledge Base List
* [~~AddDocumentationToKnowledgeBase~~](#adddocumentationtoknowledgebase) - Add To Knowledge Base :warning: **Deprecated**
* [CreateURLDocumentRoute](#createurldocumentroute) - Create Url Document
* [CreateFileDocumentRoute](#createfiledocumentroute) - Create File Document
* [CreateTextDocumentRoute](#createtextdocumentroute) - Create Text Document
* [GetDocumentationFromKnowledgeBase](#getdocumentationfromknowledgebase) - Get Documentation From Knowledge Base
* [DeleteKnowledgeBaseDocument](#deleteknowledgebasedocument) - Delete Knowledge Base Document Or Folder
* [UpdateDocumentRoute](#updatedocumentroute) - Update Document
* [GetRagIndexOverview](#getragindexoverview) - Get Rag Index Overview.
* [GetOrCreateRagIndexes](#getorcreateragindexes) - Compute Rag Indexes In Batch
* [RefreshURLDocumentRoute](#refreshurldocumentroute) - Refresh Url Document Content
* [GetRagIndexes](#getragindexes) - Get Rag Indexes Of The Specified Knowledgebase Document.
* [RagIndexStatus](#ragindexstatus) - Compute Rag Index.
* [DeleteRagIndex](#deleteragindex) - Delete Rag Index.
* [SearchKnowledgeBaseContentRoute](#searchknowledgebasecontentroute) - Search Knowledge Base Content
* [GetKnowledgeBaseDependentAgents](#getknowledgebasedependentagents) - Get Dependent Agents List
* [GetKnowledgeBaseContent](#getknowledgebasecontent) - Get Document Content
* [GetKnowledgeBaseSourceFileURL](#getknowledgebasesourcefileurl) - Get Document Source File Url
* [GetDocumentationChunkFromKnowledgeBase](#getdocumentationchunkfromknowledgebase) - Get Documentation Chunk From Knowledge Base
* [GetToolsRoute](#gettoolsroute) - Get Tools
* [AddToolRoute](#addtoolroute) - Add Tool
* [GetToolRoute](#gettoolroute) - Get Tool
* [DeleteToolRoute](#deletetoolroute) - Delete Tool
* [UpdateToolRoute](#updatetoolroute) - Update Tool
* [GetToolDependentAgentsRoute](#gettooldependentagentsroute) - Get Dependent Agents List
* [GetSettingsRoute](#getsettingsroute) - Get Convai Settings
* [UpdateSettingsRoute](#updatesettingsroute) - Update Convai Settings
* [GetDashboardSettingsRoute](#getdashboardsettingsroute) - Get Convai Dashboard Settings
* [UpdateDashboardSettingsRoute](#updatedashboardsettingsroute) - Update Convai Dashboard Settings
* [GetSecretsRoute](#getsecretsroute) - Get Convai Workspace Secrets
* [CreateSecretRoute](#createsecretroute) - Create Convai Workspace Secret
* [DeleteSecretRoute](#deletesecretroute) - Delete Convai Workspace Secret
* [UpdateSecretRoute](#updatesecretroute) - Update Convai Workspace Secret
* [CreateBatchCall](#createbatchcall) - Submit A Batch Call Request.
* [GetWorkspaceBatchCalls](#getworkspacebatchcalls) - Get All Batch Calls For A Workspace.
* [GetBatchCall](#getbatchcall) - Get A Batch Call By Id.
* [DeleteBatchCall](#deletebatchcall) - Delete A Batch Call.
* [CancelBatchCall](#cancelbatchcall) - Cancel A Batch Call.
* [RetryBatchCall](#retrybatchcall) - Retry A Batch Call.
* [HandleSipTrunkOutboundCall](#handlesiptrunkoutboundcall) - Handle An Outbound Call Via Sip Trunk
* [ListMcpServersRoute](#listmcpserversroute) - List Mcp Servers
* [CreateMcpServerRoute](#createmcpserverroute) - Create Mcp Server
* [GetMcpRoute](#getmcproute) - Get Mcp Server
* [DeleteMcpServerRoute](#deletemcpserverroute) - Delete Mcp Server
* [UpdateMcpServerConfigRoute](#updatemcpserverconfigroute) - Update Mcp Server Configuration
* [ListMcpServerToolsRoute](#listmcpservertoolsroute) - List Mcp Server Tools
* [~~UpdateMcpServerApprovalPolicyRoute~~](#updatemcpserverapprovalpolicyroute) - Update Mcp Server Approval Policy :warning: **Deprecated**
* [AddMcpServerToolApprovalRoute](#addmcpservertoolapprovalroute) - Create Mcp Server Tool Approval
* [RemoveMcpServerToolApprovalRoute](#removemcpservertoolapprovalroute) - Delete Mcp Server Tool Approval
* [AddMcpToolConfigOverrideRoute](#addmcptoolconfigoverrideroute) - Create Mcp Tool Configuration Override
* [GetMcpToolConfigOverrideRoute](#getmcptoolconfigoverrideroute) - Get Mcp Tool Configuration Override
* [RemoveMcpToolConfigOverrideRoute](#removemcptoolconfigoverrideroute) - Delete Mcp Tool Configuration Override
* [UpdateMcpToolConfigOverrideRoute](#updatemcptoolconfigoverrideroute) - Update Mcp Tool Configuration Override
* [GetWhatsappAccount](#getwhatsappaccount) - Get Whatsapp Account
* [DeleteWhatsappAccount](#deletewhatsappaccount) - Delete Whatsapp Account
* [UpdateWhatsappAccount](#updatewhatsappaccount) - Update Whatsapp Account
* [ListWhatsappAccounts](#listwhatsappaccounts) - List Whatsapp Accounts
* [GetBranchesRoute](#getbranchesroute) - List Agent Branches
* [CreateBranchRoute](#createbranchroute) - Create A New Branch
* [GetBranchRoute](#getbranchroute) - Get Agent Branch
* [UpdateBranchRoute](#updatebranchroute) - Update Agent Branch
* [MergeBranchIntoTarget](#mergebranchintotarget) - Merge A Branch Into A Target Branch
* [CreateAgentDeploymentRoute](#createagentdeploymentroute) - Create Or Update Deployments
* [CreateAgentDraftRoute](#createagentdraftroute) - Create Agent Draft
* [DeleteAgentDraftRoute](#deleteagentdraftroute) - Delete Agent Draft
* [ListEnvironmentVariables](#listenvironmentvariables) - List Environment Variables
* [CreateEnvironmentVariable](#createenvironmentvariable) - Create Environment Variable
* [GetEnvironmentVariable](#getenvironmentvariable) - Get Environment Variable
* [UpdateEnvironmentVariable](#updateenvironmentvariable) - Update Environment Variable

## GetConversationSignedLink

Get a signed url to start a conversation with an agent with an agent that requires authorization

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_signed_link" method="get" path="/v1/convai/conversation/get-signed-url" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetConversationSignedLink(ctx, operations.GetConversationSignedLinkRequest{
        AgentID: "21m00Tcm4TlvDq8ikWAM",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationSignedURLResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `request`                                                                                                  | [operations.GetConversationSignedLinkRequest](../../models/operations/getconversationsignedlinkrequest.md) | :heavy_check_mark:                                                                                         | The request object to use for the request.                                                                 |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

### Response

**[*operations.GetConversationSignedLinkResponse](../../models/operations/getconversationsignedlinkresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ~~GetSignedURLDeprecated~~

Get a signed url to start a conversation with an agent with an agent that requires authorization

> :warning: **DEPRECATED**: This will be removed in a future release, please migrate away from it as soon as possible.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_signed_url_deprecated" method="get" path="/v1/convai/conversation/get_signed_url" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetSignedURLDeprecated(ctx, operations.GetSignedURLDeprecatedRequest{
        AgentID: "21m00Tcm4TlvDq8ikWAM",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationSignedURLResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                            | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                | :heavy_check_mark:                                                                                   | The context to use for the request.                                                                  |
| `request`                                                                                            | [operations.GetSignedURLDeprecatedRequest](../../models/operations/getsignedurldeprecatedrequest.md) | :heavy_check_mark:                                                                                   | The request object to use for the request.                                                           |
| `opts`                                                                                               | [][operations.Option](../../models/operations/option.md)                                             | :heavy_minus_sign:                                                                                   | The options for this request.                                                                        |

### Response

**[*operations.GetSignedURLDeprecatedResponse](../../models/operations/getsignedurldeprecatedresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetLivekitToken

Get a WebRTC session token for real-time communication.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_livekit_token" method="get" path="/v1/convai/conversation/token" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetLivekitToken(ctx, operations.GetLivekitTokenRequest{
        AgentID: "21m00Tcm4TlvDq8ikWAM",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.TokenResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                              | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `ctx`                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                  | :heavy_check_mark:                                                                     | The context to use for the request.                                                    |
| `request`                                                                              | [operations.GetLivekitTokenRequest](../../models/operations/getlivekittokenrequest.md) | :heavy_check_mark:                                                                     | The request object to use for the request.                                             |
| `opts`                                                                                 | [][operations.Option](../../models/operations/option.md)                               | :heavy_minus_sign:                                                                     | The options for this request.                                                          |

### Response

**[*operations.GetLivekitTokenResponse](../../models/operations/getlivekittokenresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## HandleTwilioOutboundCall

Handle an outbound call via Twilio

### Example Usage

<!-- UsageSnippet language="go" operationID="handle_twilio_outbound_call" method="post" path="/v1/convai/twilio/outbound-call" -->
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

    res, err := s.AgentsPlatform.HandleTwilioOutboundCall(ctx, components.BodyHandleAnOutboundCallViaTwilioV1ConvaiTwilioOutboundCallPost{
        AgentID: "<id>",
        AgentPhoneNumberID: "<id>",
        ToNumber: "<value>",
        ConversationInitiationClientData: optionalnullable.From(&components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Turn: optionalnullable.From(&components.TurnConfigOverride{
                    SoftTimeoutConfig: optionalnullable.From(&components.SoftTimeoutConfigOverride{
                        Message: optionalnullable.From(elevenlabsgo.Pointer("Hhmmmm...yeah.")),
                    }),
                }),
                Tts: optionalnullable.From(&components.TTSConversationalConfigOverride{
                    VoiceID: optionalnullable.From(elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal")),
                    Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
                    Speed: optionalnullable.From(elevenlabsgo.Pointer[float64](1.0)),
                    SimilarityBoost: optionalnullable.From(elevenlabsgo.Pointer[float64](0.8)),
                }),
                Agent: optionalnullable.From(&components.AgentConfigOverrideInput{
                    FirstMessage: optionalnullable.From(elevenlabsgo.Pointer("Hello, how can I help you today?")),
                    Language: optionalnullable.From(elevenlabsgo.Pointer("en")),
                    Prompt: optionalnullable.From(&components.PromptAgentAPIModelOverrideInput{
                        Prompt: optionalnullable.From(elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation.")),
                        Llm: optionalnullable.From(elevenlabsgo.Pointer(components.LlmGemini20Flash001)),
                        ToolIds: optionalnullable.From(elevenlabsgo.Pointer([]string{})),
                        KnowledgeBase: optionalnullable.From(elevenlabsgo.Pointer([]components.KnowledgeBaseLocator{})),
                    }),
                }),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.TwilioOutboundCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                | Type                                                                                                                                                                     | Required                                                                                                                                                                 | Description                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                    | :heavy_check_mark:                                                                                                                                                       | The context to use for the request.                                                                                                                                      |
| `body`                                                                                                                                                                   | [components.BodyHandleAnOutboundCallViaTwilioV1ConvaiTwilioOutboundCallPost](../../models/components/bodyhandleanoutboundcallviatwiliov1convaitwiliooutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                       | N/A                                                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                                              | :heavy_minus_sign:                                                                                                                                                       | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                |
| `opts`                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                 | :heavy_minus_sign:                                                                                                                                                       | The options for this request.                                                                                                                                            |

### Response

**[*operations.HandleTwilioOutboundCallResponse](../../models/operations/handletwiliooutboundcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RegisterTwilioCall

Register a Twilio call and return TwiML to connect the call

### Example Usage

<!-- UsageSnippet language="go" operationID="register_twilio_call" method="post" path="/v1/convai/twilio/register-call" -->
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

    res, err := s.AgentsPlatform.RegisterTwilioCall(ctx, components.BodyRegisterATwilioCallAndReturnTwiMLV1ConvaiTwilioRegisterCallPost{
        AgentID: "<id>",
        FromNumber: "<value>",
        ToNumber: "<value>",
        ConversationInitiationClientData: optionalnullable.From(&components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Turn: optionalnullable.From(&components.TurnConfigOverride{
                    SoftTimeoutConfig: optionalnullable.From(&components.SoftTimeoutConfigOverride{
                        Message: optionalnullable.From(elevenlabsgo.Pointer("Hhmmmm...yeah.")),
                    }),
                }),
                Tts: optionalnullable.From(&components.TTSConversationalConfigOverride{
                    VoiceID: optionalnullable.From(elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal")),
                    Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
                    Speed: optionalnullable.From(elevenlabsgo.Pointer[float64](1.0)),
                    SimilarityBoost: optionalnullable.From(elevenlabsgo.Pointer[float64](0.8)),
                }),
                Agent: optionalnullable.From(&components.AgentConfigOverrideInput{
                    FirstMessage: optionalnullable.From(elevenlabsgo.Pointer("Hello, how can I help you today?")),
                    Language: optionalnullable.From(elevenlabsgo.Pointer("en")),
                    Prompt: optionalnullable.From(&components.PromptAgentAPIModelOverrideInput{
                        Prompt: optionalnullable.From(elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation.")),
                        Llm: optionalnullable.From(elevenlabsgo.Pointer(components.LlmGemini20Flash001)),
                        ToolIds: optionalnullable.From(elevenlabsgo.Pointer([]string{})),
                        KnowledgeBase: optionalnullable.From(elevenlabsgo.Pointer([]components.KnowledgeBaseLocator{})),
                    }),
                }),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                        | Type                                                                                                                                                                             | Required                                                                                                                                                                         | Description                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                            | :heavy_check_mark:                                                                                                                                                               | The context to use for the request.                                                                                                                                              |
| `body`                                                                                                                                                                           | [components.BodyRegisterATwilioCallAndReturnTwiMLV1ConvaiTwilioRegisterCallPost](../../models/components/bodyregisteratwiliocallandreturntwimlv1convaitwilioregistercallpost.md) | :heavy_check_mark:                                                                                                                                                               | N/A                                                                                                                                                                              |
| `xiAPIKey`                                                                                                                                                                       | optionalnullable.OptionalNullable[`string`]                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                               | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                        |
| `opts`                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                         | :heavy_minus_sign:                                                                                                                                                               | The options for this request.                                                                                                                                                    |

### Response

**[*operations.RegisterTwilioCallResponse](../../models/operations/registertwiliocallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## WhatsappOutboundCall

Make an outbound call via WhatsApp

### Example Usage

<!-- UsageSnippet language="go" operationID="whatsapp_outbound_call" method="post" path="/v1/convai/whatsapp/outbound-call" -->
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

    res, err := s.AgentsPlatform.WhatsappOutboundCall(ctx, components.BodyMakeAnOutboundCallViaWhatsAppV1ConvaiWhatsappOutboundCallPost{
        WhatsappPhoneNumberID: "<id>",
        WhatsappUserID: "<id>",
        WhatsappCallPermissionRequestTemplateName: "<value>",
        WhatsappCallPermissionRequestTemplateLanguageCode: "<value>",
        AgentID: "<id>",
        ConversationInitiationClientData: optionalnullable.From(&components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Turn: optionalnullable.From(&components.TurnConfigOverride{
                    SoftTimeoutConfig: optionalnullable.From(&components.SoftTimeoutConfigOverride{
                        Message: optionalnullable.From(elevenlabsgo.Pointer("Hhmmmm...yeah.")),
                    }),
                }),
                Tts: optionalnullable.From(&components.TTSConversationalConfigOverride{
                    VoiceID: optionalnullable.From(elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal")),
                    Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
                    Speed: optionalnullable.From(elevenlabsgo.Pointer[float64](1.0)),
                    SimilarityBoost: optionalnullable.From(elevenlabsgo.Pointer[float64](0.8)),
                }),
                Agent: optionalnullable.From(&components.AgentConfigOverrideInput{
                    FirstMessage: optionalnullable.From(elevenlabsgo.Pointer("Hello, how can I help you today?")),
                    Language: optionalnullable.From(elevenlabsgo.Pointer("en")),
                    Prompt: optionalnullable.From(&components.PromptAgentAPIModelOverrideInput{
                        Prompt: optionalnullable.From(elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation.")),
                        Llm: optionalnullable.From(elevenlabsgo.Pointer(components.LlmGemini20Flash001)),
                        ToolIds: optionalnullable.From(elevenlabsgo.Pointer([]string{})),
                        KnowledgeBase: optionalnullable.From(elevenlabsgo.Pointer([]components.KnowledgeBaseLocator{})),
                    }),
                }),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.WhatsAppOutboundCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                    | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                        | :heavy_check_mark:                                                                                                                                                           | The context to use for the request.                                                                                                                                          |
| `body`                                                                                                                                                                       | [components.BodyMakeAnOutboundCallViaWhatsAppV1ConvaiWhatsappOutboundCallPost](../../models/components/bodymakeanoutboundcallviawhatsappv1convaiwhatsappoutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `xiAPIKey`                                                                                                                                                                   | optionalnullable.OptionalNullable[`string`]                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                           | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                    |
| `opts`                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | The options for this request.                                                                                                                                                |

### Response

**[*operations.WhatsappOutboundCallResponse](../../models/operations/whatsappoutboundcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## WhatsappOutboundMessage

Send an outbound message via WhatsApp

### Example Usage

<!-- UsageSnippet language="go" operationID="whatsapp_outbound_message" method="post" path="/v1/convai/whatsapp/outbound-message" -->
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

    res, err := s.AgentsPlatform.WhatsappOutboundMessage(ctx, components.BodySendAnOutboundMessageViaWhatsAppV1ConvaiWhatsappOutboundMessagePost{
        WhatsappPhoneNumberID: "<id>",
        WhatsappUserID: "<id>",
        TemplateName: "<value>",
        TemplateLanguageCode: "<value>",
        TemplateParams: []components.TemplateParam{},
        AgentID: "<id>",
        ConversationInitiationClientData: optionalnullable.From(&components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Turn: optionalnullable.From(&components.TurnConfigOverride{
                    SoftTimeoutConfig: optionalnullable.From(&components.SoftTimeoutConfigOverride{
                        Message: optionalnullable.From(elevenlabsgo.Pointer("Hhmmmm...yeah.")),
                    }),
                }),
                Tts: optionalnullable.From(&components.TTSConversationalConfigOverride{
                    VoiceID: optionalnullable.From(elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal")),
                    Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
                    Speed: optionalnullable.From(elevenlabsgo.Pointer[float64](1.0)),
                    SimilarityBoost: optionalnullable.From(elevenlabsgo.Pointer[float64](0.8)),
                }),
                Agent: optionalnullable.From(&components.AgentConfigOverrideInput{
                    FirstMessage: optionalnullable.From(elevenlabsgo.Pointer("Hello, how can I help you today?")),
                    Language: optionalnullable.From(elevenlabsgo.Pointer("en")),
                    Prompt: optionalnullable.From(&components.PromptAgentAPIModelOverrideInput{
                        Prompt: optionalnullable.From(elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation.")),
                        Llm: optionalnullable.From(elevenlabsgo.Pointer(components.LlmGemini20Flash001)),
                        ToolIds: optionalnullable.From(elevenlabsgo.Pointer([]string{})),
                        KnowledgeBase: optionalnullable.From(elevenlabsgo.Pointer([]components.KnowledgeBaseLocator{})),
                    }),
                }),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.WhatsAppOutboundMessageResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                | Type                                                                                                                                                                                     | Required                                                                                                                                                                                 | Description                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                       | The context to use for the request.                                                                                                                                                      |
| `body`                                                                                                                                                                                   | [components.BodySendAnOutboundMessageViaWhatsAppV1ConvaiWhatsappOutboundMessagePost](../../models/components/bodysendanoutboundmessageviawhatsappv1convaiwhatsappoutboundmessagepost.md) | :heavy_check_mark:                                                                                                                                                                       | N/A                                                                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                       | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                |
| `opts`                                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                       | The options for this request.                                                                                                                                                            |

### Response

**[*operations.WhatsappOutboundMessageResponse](../../models/operations/whatsappoutboundmessageresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentRoute

Create an agent from a config object

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_route" method="post" path="/v1/convai/agents/create" -->
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

    res, err := s.AgentsPlatform.CreateAgentRoute(ctx, components.BodyCreateAgentV1ConvaiAgentsCreatePost{
        ConversationConfig: components.ConversationalConfigAPIModelInput{
            Asr: &components.ASRConversationalConfig{
                Keywords: []string{
                    "hello",
                    "world",
                },
            },
            Turn: &components.TurnConfig{
                SoftTimeoutConfig: &components.SoftTimeoutConfig{},
            },
            Tts: &components.TTSConversationalConfigInput{
                ModelID: components.TTSConversationalModelElevenTurboV2.ToPointer(),
                OptimizeStreamingLatency: components.TTSOptimizeStreamingLatencyThree.ToPointer(),
                PronunciationDictionaryLocators: []components.PydanticPronunciationDictionaryVersionLocator{},
            },
            Conversation: &components.ConversationConfig{
                ClientEvents: []components.ClientEvent{
                    components.ClientEventAudio,
                    components.ClientEventInterruption,
                },
            },
            LanguagePresets: map[string]components.LanguagePresetInput{
                "key": components.LanguagePresetInput{
                    Overrides: components.ConversationConfigClientOverrideInput{
                        Turn: optionalnullable.From(&components.TurnConfigOverride{
                            SoftTimeoutConfig: optionalnullable.From(&components.SoftTimeoutConfigOverride{
                                Message: optionalnullable.From(elevenlabsgo.Pointer("Hhmmmm...yeah.")),
                            }),
                        }),
                        Tts: optionalnullable.From(&components.TTSConversationalConfigOverride{
                            VoiceID: optionalnullable.From(elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal")),
                            Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
                            Speed: optionalnullable.From(elevenlabsgo.Pointer[float64](1.0)),
                            SimilarityBoost: optionalnullable.From(elevenlabsgo.Pointer[float64](0.8)),
                        }),
                        Agent: optionalnullable.From(&components.AgentConfigOverrideInput{
                            FirstMessage: optionalnullable.From(elevenlabsgo.Pointer("Hello, how can I help you today?")),
                            Language: optionalnullable.From(elevenlabsgo.Pointer("en")),
                            Prompt: optionalnullable.From(&components.PromptAgentAPIModelOverrideInput{
                                Prompt: optionalnullable.From(elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation.")),
                                Llm: optionalnullable.From(elevenlabsgo.Pointer(components.LlmGemini20Flash001)),
                                ToolIds: optionalnullable.From(elevenlabsgo.Pointer([]string{})),
                                KnowledgeBase: optionalnullable.From(elevenlabsgo.Pointer([]components.KnowledgeBaseLocator{})),
                            }),
                        }),
                    },
                },
            },
            Vad: &components.VADConfig{},
            Agent: &components.AgentConfigAPIModelInput{
                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
            },
        },
        PlatformSettings: optionalnullable.From(&components.AgentPlatformSettingsRequestModel{
            Evaluation: &components.EvaluationSettingsInput{
                Criteria: []components.PromptEvaluationCriteria{
                    components.PromptEvaluationCriteria{
                        ID: "1234567890",
                        Name: "Customer satisfaction check",
                        ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
                    },
                },
            },
            Widget: &components.WidgetConfigInput{
                CustomAvatarPath: optionalnullable.From(elevenlabsgo.Pointer("https://example.com/avatar.png")),
            },
            DataCollection: map[string]components.LiteralJSONSchemaProperty{
                "key": components.LiteralJSONSchemaProperty{
                    Type: components.LiteralJSONSchemaPropertyTypeString,
                    Description: elevenlabsgo.Pointer("A user-provided message"),
                },
            },
            Overrides: &components.ConversationInitiationClientDataConfigInput{
                CustomLlmExtraBody: elevenlabsgo.Pointer(true),
                EnableConversationInitiationClientDataFromWebhook: elevenlabsgo.Pointer(true),
            },
            WorkspaceOverrides: &components.AgentWorkspaceOverridesInput{
                ConversationInitiationClientDataWebhook: optionalnullable.From(&components.ConversationInitiationClientDataWebhook{
                    URL: "https://example.com/webhook",
                    RequestHeaders: map[string]components.ConversationInitiationClientDataWebhookRequestHeaders{
                        "Content-Type": components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(
                            "application/json",
                        ),
                    },
                }),
            },
            Testing: &components.AgentTestingSettings{
                AttachedTests: []components.AttachedTestModel{
                    components.AttachedTestModel{
                        TestID: "test_123",
                        WorkflowNodeID: optionalnullable.From(elevenlabsgo.Pointer("node_abc")),
                    },
                    components.AttachedTestModel{
                        TestID: "test_456",
                    },
                },
            },
            Auth: &components.AuthSettings{
                EnableAuth: elevenlabsgo.Pointer(true),
                Allowlist: []components.AllowlistItem{
                    components.AllowlistItem{
                        Hostname: "https://example.com",
                    },
                },
                RequireOriginHeader: elevenlabsgo.Pointer(true),
                ShareableToken: optionalnullable.From(elevenlabsgo.Pointer("1234567890")),
            },
            CallLimits: &components.AgentCallLimits{},
            Privacy: &components.PrivacyConfigInput{},
        }),
        Workflow: &components.AgentWorkflowRequestModel{
            Edges: map[string]components.WorkflowEdgeModelInput{
                "entry_to_tool_a": components.WorkflowEdgeModelInput{
                    Source: "entry_node",
                    Target: "tool_node_a",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    ))),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    ))),
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    ))),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: true,
                        },
                    ))),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    ))),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputStringLiteral(
                                components.ASTStringNodeInput{
                                    Value: "<value>",
                                },
                            ),
                        },
                    ))),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
            },
            Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                "entry_node": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
                "failure_node": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                    components.WorkflowPhoneNumberNodeModelInput{
                        TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationPhoneDynamicVariable(
                            components.PhoneNumberDynamicVariableTransferDestination{
                                PhoneNumber: "1-277-946-5331 x002",
                            },
                        ),
                    },
                ),
                "start_node": components.CreateAgentWorkflowRequestModelNodesStart(
                    components.WorkflowStartNodeModelInput{},
                ),
                "success_conversation": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: "<id>",
                    },
                ),
                "success_end": components.CreateAgentWorkflowRequestModelNodesTool(
                    components.WorkflowToolNodeModelInput{},
                ),
                "success_phone": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
                "success_transfer": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                    components.WorkflowOverrideAgentNodeModelInput{
                        Label: "<value>",
                    },
                ),
                "tool_node_a": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
                "tool_node_b": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                    components.WorkflowPhoneNumberNodeModelInput{
                        TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationSipURI(
                            components.SIPURITransferDestination{
                                SipURI: "https://concerned-cuckoo.com/",
                            },
                        ),
                    },
                ),
            },
        },
        Name: optionalnullable.From(elevenlabsgo.Pointer("My agent")),
        Tags: optionalnullable.From(elevenlabsgo.Pointer([]string{
            "Customer Support",
            "Technical Help",
            "Eleven",
        })),
    }, elevenlabsgo.Pointer(false), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.BodyCreateAgentV1ConvaiAgentsCreatePost](../../models/components/bodycreateagentv1convaiagentscreatepost.md)                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `enableVersioning`                                                                                                                                        | `*bool`                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                        | Enable versioning for the agent                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateAgentRouteResponse](../../models/operations/createagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentSummariesRoute

Returns summaries for the specified agents.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_summaries_route" method="get" path="/v1/convai/agents/summaries" -->
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

    res, err := s.AgentsPlatform.GetAgentSummariesRoute(ctx, []string{
        "J3Pbu5gP6NNKBscdCdwB",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetAgentSummariesV1ConvaiAgentsSummariesGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentIds`                                                                                                                                                | []`string`                                                                                                                                                | :heavy_check_mark:                                                                                                                                        | List of agent IDs to fetch summaries for                                                                                                                  | **Example 1:** J3Pbu5gP6NNKBscdCdwB<br/>**Example 2:** K4Qcu6hQ7OOLCtdeDeXC                                                                               |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAgentSummariesRouteResponse](../../models/operations/getagentsummariesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentRoute

Retrieve config for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_route" method="get" path="/v1/convai/agents/{agent_id}" -->
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

    res, err := s.AgentsPlatform.GetAgentRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", optionalnullable.From(elevenlabsgo.Pointer("agtvrsn_8901k4t9z5defmb8vh3e9361y7nj")), optionalnullable.From(elevenlabsgo.Pointer("agtbranch_0901k4aafjxxfxt93gd841r7tv5t")), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `versionID`                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | The ID of the agent version to use                                                                                                                        | agtvrsn_8901k4t9z5defmb8vh3e9361y7nj                                                                                                                      |
| `branchID`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | The ID of the branch to use                                                                                                                               | agtbranch_0901k4aafjxxfxt93gd841r7tv5t                                                                                                                    |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAgentRouteResponse](../../models/operations/getagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAgentRoute

Delete an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_agent_route" method="delete" path="/v1/convai/agents/{agent_id}" -->
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

    res, err := s.AgentsPlatform.DeleteAgentRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeleteAgentRouteResponse](../../models/operations/deleteagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PatchAgentSettingsRoute

Patches an Agent settings

### Example Usage

<!-- UsageSnippet language="go" operationID="patch_agent_settings_route" method="patch" path="/v1/convai/agents/{agent_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.PatchAgentSettingsRoute(ctx, operations.PatchAgentSettingsRouteRequest{
        AgentID: "agent_3701k3ttaq12ewp8b7qv5rfyszkz",
        BranchID: optionalnullable.From(elevenlabsgo.Pointer("agtbranch_0901k4aafjxxfxt93gd841r7tv5t")),
        Body: &components.BodyPatchesAnAgentSettingsV1ConvaiAgentsAgentIDPatch{
            Workflow: &components.AgentWorkflowRequestModel{
                Edges: map[string]components.WorkflowEdgeModelInput{
                    "entry_to_tool_a": components.WorkflowEdgeModelInput{
                        Source: "entry_node",
                        Target: "tool_node_a",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        ))),
                    },
                    "start_to_entry": components.WorkflowEdgeModelInput{
                        Source: "start_node",
                        Target: "entry_node",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        ))),
                    },
                    "tool_a_to_failure": components.WorkflowEdgeModelInput{
                        Source: "tool_node_a",
                        Target: "failure_node",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                            components.WorkflowUnconditionalModelInput{},
                        ))),
                    },
                    "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                        Source: "tool_node_a",
                        Target: "tool_node_b",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        ))),
                    },
                    "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_transfer",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: false,
                            },
                        ))),
                    },
                    "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_conversation",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                            components.WorkflowLLMConditionModelInput{
                                Condition: "User's last message contains a question about our pricing.",
                            },
                        ))),
                    },
                    "tool_b_to_end": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_end",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: false,
                            },
                        ))),
                    },
                    "tool_b_to_phone": components.WorkflowEdgeModelInput{
                        Source: "tool_node_b",
                        Target: "success_phone",
                        ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                            components.WorkflowResultConditionModelInput{
                                Successful: true,
                            },
                        ))),
                    },
                },
                Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                    "entry_node": components.CreateAgentWorkflowRequestModelNodesEnd(
                        components.WorkflowEndNodeModelInput{},
                    ),
                    "failure_node": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "start_node": components.CreateAgentWorkflowRequestModelNodesEnd(
                        components.WorkflowEndNodeModelInput{},
                    ),
                    "success_conversation": components.CreateAgentWorkflowRequestModelNodesStart(
                        components.WorkflowStartNodeModelInput{},
                    ),
                    "success_end": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                        components.WorkflowStandaloneAgentNodeModelInput{
                            AgentID: "<id>",
                        },
                    ),
                    "success_phone": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                    "success_transfer": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                        components.WorkflowStandaloneAgentNodeModelInput{
                            AgentID: "<id>",
                        },
                    ),
                    "tool_node_a": components.CreateAgentWorkflowRequestModelNodesEnd(
                        components.WorkflowEndNodeModelInput{},
                    ),
                    "tool_node_b": components.CreateAgentWorkflowRequestModelNodesTool(
                        components.WorkflowToolNodeModelInput{},
                    ),
                },
            },
            Name: optionalnullable.From(elevenlabsgo.Pointer("My agent")),
            Tags: optionalnullable.From(elevenlabsgo.Pointer([]string{
                "Customer Support",
                "Technical Help",
                "Eleven",
            })),
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |
| `request`                                                                                              | [operations.PatchAgentSettingsRouteRequest](../../models/operations/patchagentsettingsrouterequest.md) | :heavy_check_mark:                                                                                     | The request object to use for the request.                                                             |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |

### Response

**[*operations.PatchAgentSettingsRouteResponse](../../models/operations/patchagentsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentWidgetRoute

Retrieve the widget configuration for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_widget_route" method="get" path="/v1/convai/agents/{agent_id}/widget" -->
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

    res, err := s.AgentsPlatform.GetAgentWidgetRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", optionalnullable.From[string](nil), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentEmbedResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                       | Type                                                                                                                                                            | Required                                                                                                                                                        | Description                                                                                                                                                     | Example                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                           | [context.Context](https://pkg.go.dev/context#Context)                                                                                                           | :heavy_check_mark:                                                                                                                                              | The context to use for the request.                                                                                                                             |                                                                                                                                                                 |
| `agentID`                                                                                                                                                       | `string`                                                                                                                                                        | :heavy_check_mark:                                                                                                                                              | The id of an agent. This is returned on agent creation.                                                                                                         | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                              |
| `conversationSignature`                                                                                                                                         | optionalnullable.OptionalNullable[`string`]                                                                                                                     | :heavy_minus_sign:                                                                                                                                              | An expiring token that enables a websocket conversation to start. These can be generated for an agent using the /v1/convai/conversation/get-signed-url endpoint |                                                                                                                                                                 |
| `xiAPIKey`                                                                                                                                                      | optionalnullable.OptionalNullable[`string`]                                                                                                                     | :heavy_minus_sign:                                                                                                                                              | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.       |                                                                                                                                                                 |
| `opts`                                                                                                                                                          | [][operations.Option](../../models/operations/option.md)                                                                                                        | :heavy_minus_sign:                                                                                                                                              | The options for this request.                                                                                                                                   |                                                                                                                                                                 |

### Response

**[*operations.GetAgentWidgetRouteResponse](../../models/operations/getagentwidgetrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentLinkRoute

Get the current link used to share the agent with others

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_link_route" method="get" path="/v1/convai/agents/{agent_id}/link" -->
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

    res, err := s.AgentsPlatform.GetAgentLinkRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentLinkResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAgentLinkRouteResponse](../../models/operations/getagentlinkrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PostAgentAvatarRoute

Sets the avatar for an agent displayed in the widget

### Example Usage

<!-- UsageSnippet language="go" operationID="post_agent_avatar_route" method="post" path="/v1/convai/agents/{agent_id}/avatar" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.PostAgentAvatarRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodyPostAgentAvatarV1ConvaiAgentsAgentIDAvatarPost{
        AvatarFile: components.AvatarFile{
            FileName: "example.file",
            Content: example,
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.PostAgentAvatarResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `body`                                                                                                                                                    | [components.BodyPostAgentAvatarV1ConvaiAgentsAgentIDAvatarPost](../../models/components/bodypostagentavatarv1convaiagentsagentidavatarpost.md)            | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.PostAgentAvatarRouteResponse](../../models/operations/postagentavatarrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentsRoute

Returns a list of your agents and their metadata.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agents_route" method="get" path="/v1/convai/agents" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetAgentsRoute(ctx, operations.GetAgentsRouteRequest{
        Archived: optionalnullable.From(elevenlabsgo.Pointer(false)),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentsPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |
| `request`                                                                            | [operations.GetAgentsRouteRequest](../../models/operations/getagentsrouterequest.md) | :heavy_check_mark:                                                                   | The request object to use for the request.                                           |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |

### Response

**[*operations.GetAgentsRouteResponse](../../models/operations/getagentsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentKnowledgeBaseSize

Returns the number of pages in the agent's knowledge base.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_knowledge_base_size" method="get" path="/v1/convai/agent/{agent_id}/knowledge-base/size" -->
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

    res, err := s.AgentsPlatform.GetAgentKnowledgeBaseSize(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentKnowledgebaseSizeResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetAgentKnowledgeBaseSizeResponse](../../models/operations/getagentknowledgebasesizeresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentLlmExpectedCostCalculation

Calculates expected number of LLM tokens needed for the specified agent.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_llm_expected_cost_calculation" method="post" path="/v1/convai/agent/{agent_id}/llm-usage/calculate" -->
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

    res, err := s.AgentsPlatform.GetAgentLlmExpectedCostCalculation(ctx, "<id>", components.LLMUsageCalculatorRequestModel{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.LLMUsageCalculatorResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `body`                                                                                                                                                    | [components.LLMUsageCalculatorRequestModel](../../models/components/llmusagecalculatorrequestmodel.md)                                                    | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetAgentLlmExpectedCostCalculationResponse](../../models/operations/getagentllmexpectedcostcalculationresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DuplicateAgentRoute

Create a new agent by duplicating an existing one

### Example Usage

<!-- UsageSnippet language="go" operationID="duplicate_agent_route" method="post" path="/v1/convai/agents/{agent_id}/duplicate" -->
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

    res, err := s.AgentsPlatform.DuplicateAgentRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", optionalnullable.From[string](nil), &components.BodyDuplicateAgentV1ConvaiAgentsAgentIDDuplicatePost{
        Name: optionalnullable.From(elevenlabsgo.Pointer("My agent")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `body`                                                                                                                                                    | [*components.BodyDuplicateAgentV1ConvaiAgentsAgentIDDuplicatePost](../../models/components/bodyduplicateagentv1convaiagentsagentidduplicatepost.md)       | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DuplicateAgentRouteResponse](../../models/operations/duplicateagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RunConversationSimulationRoute

Run a conversation between the agent and a simulated user.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_simulation_route" method="post" path="/v1/convai/agents/{agent_id}/simulate-conversation" -->
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

    res, err := s.AgentsPlatform.RunConversationSimulationRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodySimulatesAConversationV1ConvaiAgentsAgentIDSimulateConversationPost{
        SimulationSpecification: components.ConversationSimulationSpecification{
            SimulatedUserConfig: components.AgentConfigAPIModelInput{
                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
            },
        },
        ExtraEvaluationCriteria: optionalnullable.From(elevenlabsgo.Pointer([]components.PromptEvaluationCriteria{
            components.PromptEvaluationCriteria{
                ID: "1234567890",
                Name: "Customer satisfaction check",
                ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
            },
        })),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AgentSimulatedChatTestResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                | Type                                                                                                                                                                                     | Required                                                                                                                                                                                 | Description                                                                                                                                                                              | Example                                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                       | The context to use for the request.                                                                                                                                                      |                                                                                                                                                                                          |
| `agentID`                                                                                                                                                                                | `string`                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                       | The id of an agent. This is returned on agent creation.                                                                                                                                  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                                                       |
| `body`                                                                                                                                                                                   | [components.BodySimulatesAConversationV1ConvaiAgentsAgentIDSimulateConversationPost](../../models/components/bodysimulatesaconversationv1convaiagentsagentidsimulateconversationpost.md) | :heavy_check_mark:                                                                                                                                                                       | N/A                                                                                                                                                                                      |                                                                                                                                                                                          |
| `xiAPIKey`                                                                                                                                                                               | optionalnullable.OptionalNullable[`string`]                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                       | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                |                                                                                                                                                                                          |
| `opts`                                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                       | The options for this request.                                                                                                                                                            |                                                                                                                                                                                          |

### Response

**[*operations.RunConversationSimulationRouteResponse](../../models/operations/runconversationsimulationrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RunConversationSimulationRouteStream

Run a conversation between the agent and a simulated user and stream back the response. Response is streamed back as partial lists of messages that should be concatenated and once the conversation has complete a single final message with the conversation analysis will be sent.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_simulation_route_stream" method="post" path="/v1/convai/agents/{agent_id}/simulate-conversation/stream" -->
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

    res, err := s.AgentsPlatform.RunConversationSimulationRouteStream(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodySimulatesAConversationStreamV1ConvaiAgentsAgentIDSimulateConversationStreamPost{
        SimulationSpecification: components.ConversationSimulationSpecification{
            SimulatedUserConfig: components.AgentConfigAPIModelInput{
                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
            },
        },
        ExtraEvaluationCriteria: optionalnullable.From(elevenlabsgo.Pointer([]components.PromptEvaluationCriteria{
            components.PromptEvaluationCriteria{
                ID: "1234567890",
                Name: "Customer satisfaction check",
                ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
            },
        })),
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

| Parameter                                                                                                                                                                                                        | Type                                                                                                                                                                                                             | Required                                                                                                                                                                                                         | Description                                                                                                                                                                                                      | Example                                                                                                                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                               | The context to use for the request.                                                                                                                                                                              |                                                                                                                                                                                                                  |
| `agentID`                                                                                                                                                                                                        | `string`                                                                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                                                               | The id of an agent. This is returned on agent creation.                                                                                                                                                          | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                                                                               |
| `body`                                                                                                                                                                                                           | [components.BodySimulatesAConversationStreamV1ConvaiAgentsAgentIDSimulateConversationStreamPost](../../models/components/bodysimulatesaconversationstreamv1convaiagentsagentidsimulateconversationstreampost.md) | :heavy_check_mark:                                                                                                                                                                                               | N/A                                                                                                                                                                                                              |                                                                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                                                                       | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                                                               | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                        |                                                                                                                                                                                                                  |
| `opts`                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                    |                                                                                                                                                                                                                  |

### Response

**[*operations.RunConversationSimulationRouteStreamResponse](../../models/operations/runconversationsimulationroutestreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentTestFolderRoute

Creates a folder for organizing agent tests.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_test_folder_route" method="post" path="/v1/convai/agent-testing/folders" -->
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

    res, err := s.AgentsPlatform.CreateAgentTestFolderRoute(ctx, components.BodyCreateAgentTestFolderV1ConvaiAgentTestingFoldersPost{
        Name: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentTestFolderResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                  | Type                                                                                                                                                       | Required                                                                                                                                                   | Description                                                                                                                                                |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                                                                      | :heavy_check_mark:                                                                                                                                         | The context to use for the request.                                                                                                                        |
| `body`                                                                                                                                                     | [components.BodyCreateAgentTestFolderV1ConvaiAgentTestingFoldersPost](../../models/components/bodycreateagenttestfolderv1convaiagenttestingfolderspost.md) | :heavy_check_mark:                                                                                                                                         | N/A                                                                                                                                                        |
| `xiAPIKey`                                                                                                                                                 | optionalnullable.OptionalNullable[`string`]                                                                                                                | :heavy_minus_sign:                                                                                                                                         | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.  |
| `opts`                                                                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                                                                   | :heavy_minus_sign:                                                                                                                                         | The options for this request.                                                                                                                              |

### Response

**[*operations.CreateAgentTestFolderRouteResponse](../../models/operations/createagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentTestFolderRoute

Gets an agent test folder by ID, including its folder path.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_test_folder_route" method="get" path="/v1/convai/agent-testing/folders/{folder_id}" -->
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

    res, err := s.AgentsPlatform.GetAgentTestFolderRoute(ctx, "tfld_7301khxdkycse5f88fzjdtrterzm", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentTestFolderResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `folderID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The folder ID.                                                                                                                                            | tfld_7301khxdkycse5f88fzjdtrterzm                                                                                                                         |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAgentTestFolderRouteResponse](../../models/operations/getagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAgentTestFolderRoute

Deletes an agent test folder by ID. Use force=true to delete a non-empty folder and all its contents.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_agent_test_folder_route" method="delete" path="/v1/convai/agent-testing/folders/{folder_id}" -->
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

    res, err := s.AgentsPlatform.DeleteAgentTestFolderRoute(ctx, "tfld_7301khxdkycse5f88fzjdtrterzm", elevenlabsgo.Pointer(false), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `folderID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The folder ID.                                                                                                                                            | tfld_7301khxdkycse5f88fzjdtrterzm                                                                                                                         |
| `force`                                                                                                                                                   | `*bool`                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                        | Force delete. Required for deleting non-empty folders.                                                                                                    |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeleteAgentTestFolderRouteResponse](../../models/operations/deleteagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateAgentTestFolderRoute

Updates an agent test folder. Currently only supports updating the folder name.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_agent_test_folder_route" method="patch" path="/v1/convai/agent-testing/folders/{folder_id}" -->
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

    res, err := s.AgentsPlatform.UpdateAgentTestFolderRoute(ctx, "tfld_7301khxdkycse5f88fzjdtrterzm", components.BodyUpdateAgentTestFolderV1ConvaiAgentTestingFoldersFolderIDPatch{
        Name: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentTestFolderResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                    | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  | Example                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                        | :heavy_check_mark:                                                                                                                                                           | The context to use for the request.                                                                                                                                          |                                                                                                                                                                              |
| `folderID`                                                                                                                                                                   | `string`                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | The folder ID.                                                                                                                                                               | tfld_7301khxdkycse5f88fzjdtrterzm                                                                                                                                            |
| `body`                                                                                                                                                                       | [components.BodyUpdateAgentTestFolderV1ConvaiAgentTestingFoldersFolderIDPatch](../../models/components/bodyupdateagenttestfolderv1convaiagenttestingfoldersfolderidpatch.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |                                                                                                                                                                              |
| `xiAPIKey`                                                                                                                                                                   | optionalnullable.OptionalNullable[`string`]                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                           | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                    |                                                                                                                                                                              |
| `opts`                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | The options for this request.                                                                                                                                                |                                                                                                                                                                              |

### Response

**[*operations.UpdateAgentTestFolderRouteResponse](../../models/operations/updateagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AgentTestingBulkMoveRoute

Moves multiple tests or folders from one folder to another.

### Example Usage

<!-- UsageSnippet language="go" operationID="agent_testing_bulk_move_route" method="post" path="/v1/convai/agent-testing/bulk-move" -->
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

    res, err := s.AgentsPlatform.AgentTestingBulkMoveRoute(ctx, components.BodyBulkMoveTestsToFolderV1ConvaiAgentTestingBulkMovePost{
        EntityIds: []string{
            "<value 1>",
            "<value 2>",
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                    | Type                                                                                                                                                         | Required                                                                                                                                                     | Description                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                        | :heavy_check_mark:                                                                                                                                           | The context to use for the request.                                                                                                                          |
| `body`                                                                                                                                                       | [components.BodyBulkMoveTestsToFolderV1ConvaiAgentTestingBulkMovePost](../../models/components/bodybulkmoveteststofolderv1convaiagenttestingbulkmovepost.md) | :heavy_check_mark:                                                                                                                                           | N/A                                                                                                                                                          |
| `xiAPIKey`                                                                                                                                                   | optionalnullable.OptionalNullable[`string`]                                                                                                                  | :heavy_minus_sign:                                                                                                                                           | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.    |
| `opts`                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                     | :heavy_minus_sign:                                                                                                                                           | The options for this request.                                                                                                                                |

### Response

**[*operations.AgentTestingBulkMoveRouteResponse](../../models/operations/agenttestingbulkmoverouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationHistoriesRoute

Get all conversations of agents that user owns. With option to restrict to a specific agent.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_histories_route" method="get" path="/v1/convai/conversations" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetConversationHistoriesRoute(ctx, operations.GetConversationHistoriesRouteRequest{
        AgentID: optionalnullable.From(elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationsPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                          | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                              | :heavy_check_mark:                                                                                                 | The context to use for the request.                                                                                |
| `request`                                                                                                          | [operations.GetConversationHistoriesRouteRequest](../../models/operations/getconversationhistoriesrouterequest.md) | :heavy_check_mark:                                                                                                 | The request object to use for the request.                                                                         |
| `opts`                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                           | :heavy_minus_sign:                                                                                                 | The options for this request.                                                                                      |

### Response

**[*operations.GetConversationHistoriesRouteResponse](../../models/operations/getconversationhistoriesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationUsersRoute

Get distinct users from conversations with pagination.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_users_route" method="get" path="/v1/convai/users" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetConversationUsersRoute(ctx, operations.GetConversationUsersRouteRequest{
        AgentID: optionalnullable.From(elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationUsersPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `request`                                                                                                  | [operations.GetConversationUsersRouteRequest](../../models/operations/getconversationusersrouterequest.md) | :heavy_check_mark:                                                                                         | The request object to use for the request.                                                                 |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

### Response

**[*operations.GetConversationUsersRouteResponse](../../models/operations/getconversationusersrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationHistoryRoute

Get the details of a particular conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_history_route" method="get" path="/v1/convai/conversations/{conversation_id}" -->
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

    res, err := s.AgentsPlatform.GetConversationHistoryRoute(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `conversationID`                                                                                                                                          | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of the conversation you're taking the action on.                                                                                                   | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetConversationHistoryRouteResponse](../../models/operations/getconversationhistoryrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteConversationRoute

Delete a particular conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_conversation_route" method="delete" path="/v1/convai/conversations/{conversation_id}" -->
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

    res, err := s.AgentsPlatform.DeleteConversationRoute(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `conversationID`                                                                                                                                          | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of the conversation you're taking the action on.                                                                                                   | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeleteConversationRouteResponse](../../models/operations/deleteconversationrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationAudioRoute

Get the audio recording of a particular conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_audio_route" method="get" path="/v1/convai/conversations/{conversation_id}/audio" -->
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

    res, err := s.AgentsPlatform.GetConversationAudioRoute(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `conversationID`                                                                                                                                          | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of the conversation you're taking the action on.                                                                                                   | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetConversationAudioRouteResponse](../../models/operations/getconversationaudiorouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PostConversationFeedbackRoute

Send the feedback for the given conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="post_conversation_feedback_route" method="post" path="/v1/convai/conversations/{conversation_id}/feedback" -->
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

    res, err := s.AgentsPlatform.PostConversationFeedbackRoute(ctx, "21m00Tcm4TlvDq8ikWAM", components.ConversationFeedbackRequestModel{
        Feedback: optionalnullable.From(elevenlabsgo.Pointer(components.UserFeedbackScoreLike)),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                | Example                                                                                                    |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |                                                                                                            |
| `conversationID`                                                                                           | `string`                                                                                                   | :heavy_check_mark:                                                                                         | The id of the conversation you're taking the action on.                                                    | 21m00Tcm4TlvDq8ikWAM                                                                                       |
| `body`                                                                                                     | [components.ConversationFeedbackRequestModel](../../models/components/conversationfeedbackrequestmodel.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        | {<br/>"feedback": "like"<br/>}                                                                             |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |                                                                                                            |

### Response

**[*operations.PostConversationFeedbackRouteResponse](../../models/operations/postconversationfeedbackrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## TextSearchConversationMessagesRoute

Search through conversation transcript messages by full-text and fuzzy search

### Example Usage

<!-- UsageSnippet language="go" operationID="text_search_conversation_messages_route" method="get" path="/v1/convai/conversations/messages/text-search" example="default" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.TextSearchConversationMessagesRoute(ctx, operations.TextSearchConversationMessagesRouteRequest{
        TextQuery: "refund policy",
        AgentID: optionalnullable.From(elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MessagesSearchResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                      | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                          | :heavy_check_mark:                                                                                                             | The context to use for the request.                                                                                            |
| `request`                                                                                                                      | [operations.TextSearchConversationMessagesRouteRequest](../../models/operations/textsearchconversationmessagesrouterequest.md) | :heavy_check_mark:                                                                                                             | The request object to use for the request.                                                                                     |
| `opts`                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                       | :heavy_minus_sign:                                                                                                             | The options for this request.                                                                                                  |

### Response

**[*operations.TextSearchConversationMessagesRouteResponse](../../models/operations/textsearchconversationmessagesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SmartSearchConversationMessagesRoute

Search conversation transcripts by semantic similarity to surface relevant messages based on meaning and intent, rather than exact keyword matches

### Example Usage

<!-- UsageSnippet language="go" operationID="smart_search_conversation_messages_route" method="get" path="/v1/convai/conversations/messages/smart-search" example="default" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.SmartSearchConversationMessagesRoute(ctx, operations.SmartSearchConversationMessagesRouteRequest{
        TextQuery: "Customer asking to cancel and get money back",
        AgentID: optionalnullable.From(elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM")),
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MessagesSearchResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                        | Type                                                                                                                             | Required                                                                                                                         | Description                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                            | :heavy_check_mark:                                                                                                               | The context to use for the request.                                                                                              |
| `request`                                                                                                                        | [operations.SmartSearchConversationMessagesRouteRequest](../../models/operations/smartsearchconversationmessagesrouterequest.md) | :heavy_check_mark:                                                                                                               | The request object to use for the request.                                                                                       |
| `opts`                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                         | :heavy_minus_sign:                                                                                                               | The options for this request.                                                                                                    |

### Response

**[*operations.SmartSearchConversationMessagesRouteResponse](../../models/operations/smartsearchconversationmessagesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListPhoneNumbersRoute

Retrieve all Phone Numbers

### Example Usage

<!-- UsageSnippet language="go" operationID="list_phone_numbers_route" method="get" path="/v1/convai/phone-numbers" -->
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

    res, err := s.AgentsPlatform.ListPhoneNumbersRoute(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseListPhoneNumbersV1ConvaiPhoneNumbersGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.ListPhoneNumbersRouteResponse](../../models/operations/listphonenumbersrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreatePhoneNumberRoute

Import Phone Number from provider configuration (Twilio or SIP trunk)

### Example Usage

<!-- UsageSnippet language="go" operationID="create_phone_number_route" method="post" path="/v1/convai/phone-numbers" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.CreatePhoneNumberRoute(ctx, operations.CreatePhoneRequestCreateTwilioPhoneNumberRequest(
        components.CreateTwilioPhoneNumberRequest{
            PhoneNumber: "1-844-780-5664",
            Label: "<value>",
            Sid: "<id>",
            Token: "<value>",
        },
    ), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreatePhoneNumberResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [operations.PhoneRequest](../../models/operations/phonerequest.md)                                                                                        | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreatePhoneNumberRouteResponse](../../models/operations/createphonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPhoneNumberRoute

Retrieve Phone Number details by ID

### Example Usage

<!-- UsageSnippet language="go" operationID="get_phone_number_route" method="get" path="/v1/convai/phone-numbers/{phone_number_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetPhoneNumberRoute(ctx, "TeaqRRdTcIfIu2i7BYfT", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet != nil {
        switch res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.Type {
            case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeTwilio:
                // res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberTwilioResponseModel is populated
            case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeSipTrunk:
                // res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberSIPTrunkResponseModel is populated
            default:
                // Unknown type - use res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `phoneNumberID`                                                                                                                                           | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | TeaqRRdTcIfIu2i7BYfT                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetPhoneNumberRouteResponse](../../models/operations/getphonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeletePhoneNumberRoute

Delete Phone Number by ID

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_phone_number_route" method="delete" path="/v1/convai/phone-numbers/{phone_number_id}" -->
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

    res, err := s.AgentsPlatform.DeletePhoneNumberRoute(ctx, "TeaqRRdTcIfIu2i7BYfT", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `phoneNumberID`                                                                                                                                           | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | TeaqRRdTcIfIu2i7BYfT                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeletePhoneNumberRouteResponse](../../models/operations/deletephonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdatePhoneNumberRoute

Update assigned agent of a phone number

### Example Usage

<!-- UsageSnippet language="go" operationID="update_phone_number_route" method="patch" path="/v1/convai/phone-numbers/{phone_number_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.UpdatePhoneNumberRoute(ctx, "TeaqRRdTcIfIu2i7BYfT", components.UpdatePhoneNumberRequest{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch != nil {
        switch res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.Type {
            case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeTwilio:
                // res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberTwilioResponseModel is populated
            case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeSipTrunk:
                // res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberSIPTrunkResponseModel is populated
            default:
                // Unknown type - use res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `phoneNumberID`                                                                                                                                           | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | TeaqRRdTcIfIu2i7BYfT                                                                                                                                      |
| `body`                                                                                                                                                    | [components.UpdatePhoneNumberRequest](../../models/components/updatephonenumberrequest.md)                                                                | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.UpdatePhoneNumberRouteResponse](../../models/operations/updatephonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPublicLlmExpectedCostCalculation

Returns a list of LLM models and the expected cost for using them based on the provided values.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_public_llm_expected_cost_calculation" method="post" path="/v1/convai/llm-usage/calculate" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetPublicLlmExpectedCostCalculation(ctx, components.LLMUsageCalculatorPublicRequestModel{
        PromptLength: 892625,
        NumberOfPages: 133936,
        RagEnabled: false,
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.LLMUsageCalculatorResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                          | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                                              | :heavy_check_mark:                                                                                                 | The context to use for the request.                                                                                |
| `request`                                                                                                          | [components.LLMUsageCalculatorPublicRequestModel](../../models/components/llmusagecalculatorpublicrequestmodel.md) | :heavy_check_mark:                                                                                                 | The request object to use for the request.                                                                         |
| `opts`                                                                                                             | [][operations.Option](../../models/operations/option.md)                                                           | :heavy_minus_sign:                                                                                                 | The options for this request.                                                                                      |

### Response

**[*operations.GetPublicLlmExpectedCostCalculationResponse](../../models/operations/getpublicllmexpectedcostcalculationresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListAvailableLlms

Returns a list of available LLM models that can be used with agents, including their capabilities and any deprecation status. The response is filtered based on the data residency of the deployment and any compliance requirements (e.g. HIPAA) of the workspace subscription.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_available_llms" method="get" path="/v1/convai/llm/list" -->
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

    res, err := s.AgentsPlatform.ListAvailableLlms(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.LLMListResponseModelInput != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.ListAvailableLlmsResponse](../../models/operations/listavailablellmsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UploadFileRoute

Upload an image or PDF file for a conversation. Returns a unique file ID that can be used to reference the file in the conversation.

### Example Usage

<!-- UsageSnippet language="go" operationID="upload_file_route" method="post" path="/v1/convai/conversations/{conversation_id}/files" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.UploadFileRoute(ctx, "<id>", components.BodyUploadFileV1ConvaiConversationsConversationIDFilesPost{
        File: components.BodyUploadFileV1ConvaiConversationsConversationIDFilesPostFile{
            FileName: "example.file",
            Content: example,
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ConvAIFileUploadResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                      | Type                                                                                                                                                           | Required                                                                                                                                                       | Description                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                                                          | :heavy_check_mark:                                                                                                                                             | The context to use for the request.                                                                                                                            |
| `conversationID`                                                                                                                                               | `string`                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `body`                                                                                                                                                         | [components.BodyUploadFileV1ConvaiConversationsConversationIDFilesPost](../../models/components/bodyuploadfilev1convaiconversationsconversationidfilespost.md) | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `xiAPIKey`                                                                                                                                                     | optionalnullable.OptionalNullable[`string`]                                                                                                                    | :heavy_minus_sign:                                                                                                                                             | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.      |
| `opts`                                                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                                                       | :heavy_minus_sign:                                                                                                                                             | The options for this request.                                                                                                                                  |

### Response

**[*operations.UploadFileRouteResponse](../../models/operations/uploadfilerouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CancelFileUploadRoute

Remove a file upload from a conversation. Only possible if the file hasn't already been used in the conversation.

### Example Usage

<!-- UsageSnippet language="go" operationID="cancel_file_upload_route" method="delete" path="/v1/convai/conversations/{conversation_id}/files/{file_id}" -->
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

    res, err := s.AgentsPlatform.CancelFileUploadRoute(ctx, "<id>", "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ConvAIFileUploadResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `fileID`                                                                                                                                                  | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `conversationID`                                                                                                                                          | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CancelFileUploadRouteResponse](../../models/operations/cancelfileuploadrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetLiveCount

Get the live count of the ongoing conversations.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_live_count" method="get" path="/v1/convai/analytics/live-count" -->
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

    res, err := s.AgentsPlatform.GetLiveCount(ctx, optionalnullable.From(elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM")), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetLiveCountResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | The id of an agent to restrict the analytics to.                                                                                                          | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetLiveCountResponse](../../models/operations/getlivecountresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentKnowledgeBaseSummariesRoute

Gets multiple knowledge base document summaries by their IDs.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_knowledge_base_summaries_route" method="get" path="/v1/convai/knowledge-base/summaries" -->
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

    res, err := s.AgentsPlatform.GetAgentKnowledgeBaseSummariesRoute(ctx, []string{
        "21m00Tcm4TlvDq8ikWAM",
        "31n11Udm5UmwEr9jkXBN",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetKnowledgeBaseSummariesByIdsV1ConvaiKnowledgeBaseSummariesGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentIds`                                                                                                                                             | []`string`                                                                                                                                                | :heavy_check_mark:                                                                                                                                        | The ids of knowledge base documents.                                                                                                                      | [<br/>"21m00Tcm4TlvDq8ikWAM",<br/>"31n11Udm5UmwEr9jkXBN"<br/>]                                                                                            |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetAgentKnowledgeBaseSummariesRouteResponse](../../models/operations/getagentknowledgebasesummariesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetKnowledgeBaseListRoute

Get a list of available knowledge base documents

### Example Usage

<!-- UsageSnippet language="go" operationID="get_knowledge_base_list_route" method="get" path="/v1/convai/knowledge-base" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetKnowledgeBaseListRoute(ctx, operations.GetKnowledgeBaseListRouteRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.GetKnowledgeBaseListResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `request`                                                                                                  | [operations.GetKnowledgeBaseListRouteRequest](../../models/operations/getknowledgebaselistrouterequest.md) | :heavy_check_mark:                                                                                         | The request object to use for the request.                                                                 |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

### Response

**[*operations.GetKnowledgeBaseListRouteResponse](../../models/operations/getknowledgebaselistrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ~~AddDocumentationToKnowledgeBase~~

Uploads a file or reference a webpage to use as part of the shared knowledge base

> :warning: **DEPRECATED**: This will be removed in a future release, please migrate away from it as soon as possible.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_documentation_to_knowledge_base" method="post" path="/v1/convai/knowledge-base" -->
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

    res, err := s.AgentsPlatform.AddDocumentationToKnowledgeBase(ctx, elevenlabsgo.Pointer(""), optionalnullable.From[string](nil), nil)
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
| `agentID`                                                                                                                                                 | `*string`                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `body`                                                                                                                                                    | [*components.BodyAddToKnowledgeBaseV1ConvaiKnowledgeBasePost](../../models/components/bodyaddtoknowledgebasev1convaiknowledgebasepost.md)                 | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.AddDocumentationToKnowledgeBaseResponse](../../models/operations/adddocumentationtoknowledgebaseresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateURLDocumentRoute

Create a knowledge base document generated by scraping the given webpage.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_url_document_route" method="post" path="/v1/convai/knowledge-base/url" -->
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

    res, err := s.AgentsPlatform.CreateURLDocumentRoute(ctx, components.BodyCreateURLDocumentV1ConvaiKnowledgeBaseURLPost{
        URL: "https://clueless-marketplace.biz/",
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
| `body`                                                                                                                                                    | [components.BodyCreateURLDocumentV1ConvaiKnowledgeBaseURLPost](../../models/components/bodycreateurldocumentv1convaiknowledgebaseurlpost.md)              | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateURLDocumentRouteResponse](../../models/operations/createurldocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateFileDocumentRoute

Create a knowledge base document generated form the uploaded file.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_file_document_route" method="post" path="/v1/convai/knowledge-base/file" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.CreateFileDocumentRoute(ctx, components.BodyCreateFileDocumentV1ConvaiKnowledgeBaseFilePost{
        File: components.BodyCreateFileDocumentV1ConvaiKnowledgeBaseFilePostFile{
            FileName: "example.file",
            Content: example,
        },
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
| `body`                                                                                                                                                    | [components.BodyCreateFileDocumentV1ConvaiKnowledgeBaseFilePost](../../models/components/bodycreatefiledocumentv1convaiknowledgebasefilepost.md)          | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateFileDocumentRouteResponse](../../models/operations/createfiledocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateTextDocumentRoute

Create a knowledge base document containing the provided text.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_text_document_route" method="post" path="/v1/convai/knowledge-base/text" -->
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

    res, err := s.AgentsPlatform.CreateTextDocumentRoute(ctx, components.BodyCreateTextDocumentV1ConvaiKnowledgeBaseTextPost{
        Text: "<value>",
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
| `body`                                                                                                                                                    | [components.BodyCreateTextDocumentV1ConvaiKnowledgeBaseTextPost](../../models/components/bodycreatetextdocumentv1convaiknowledgebasetextpost.md)          | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateTextDocumentRouteResponse](../../models/operations/createtextdocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetDocumentationFromKnowledgeBase

Get details about a specific documentation making up the agent's knowledge base

### Example Usage

<!-- UsageSnippet language="go" operationID="get_documentation_from_knowledge_base" method="get" path="/v1/convai/knowledge-base/{documentation_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetDocumentationFromKnowledgeBase(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(""), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet != nil {
        switch res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet.Type {
            case operations.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGetTypeURLObj:
                // res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet.GetKnowledgeBaseURLResponseModel is populated
            case operations.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGetTypeFile:
                // res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet.GetKnowledgeBaseFileResponseModel is populated
            case operations.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGetTypeText:
                // res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet.GetKnowledgeBaseTextResponseModel is populated
            case operations.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGetTypeFolder:
                // res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet.GetKnowledgeBaseFolderResponseModel is populated
            default:
                // Unknown type - use res.ResponseGetDocumentationFromKnowledgeBaseV1ConvaiKnowledgeBaseDocumentationIDGet.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `agentID`                                                                                                                                                 | `*string`                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetDocumentationFromKnowledgeBaseResponse](../../models/operations/getdocumentationfromknowledgebaseresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteKnowledgeBaseDocument

Delete a document or folder from the knowledge base.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_knowledge_base_document" method="delete" path="/v1/convai/knowledge-base/{documentation_id}" -->
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

    res, err := s.AgentsPlatform.DeleteKnowledgeBaseDocument(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(false), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                                             | Type                                                                                                                                                                                                                                  | Required                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                           | Example                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                                                    | The context to use for the request.                                                                                                                                                                                                   |                                                                                                                                                                                                                                       |
| `documentationID`                                                                                                                                                                                                                     | `string`                                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                                    | The id of a document from the knowledge base. This is returned on document addition.                                                                                                                                                  | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                                                                  |
| `force`                                                                                                                                                                                                                               | `*bool`                                                                                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                    | If set to true, the document or folder will be deleted regardless of whether it is used by any agents and it will be removed from the dependent agents. For non-empty folders, this will also delete all child documents and folders. |                                                                                                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                                                                                            | optionalnullable.OptionalNullable[`string`]                                                                                                                                                                                           | :heavy_minus_sign:                                                                                                                                                                                                                    | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                                                                             |                                                                                                                                                                                                                                       |
| `opts`                                                                                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                                                                    | The options for this request.                                                                                                                                                                                                         |                                                                                                                                                                                                                                       |

### Response

**[*operations.DeleteKnowledgeBaseDocumentResponse](../../models/operations/deleteknowledgebasedocumentresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateDocumentRoute

Update the name of a document

### Example Usage

<!-- UsageSnippet language="go" operationID="update_document_route" method="patch" path="/v1/convai/knowledge-base/{documentation_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.UpdateDocumentRoute(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch{
        Name: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch != nil {
        switch res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.Type {
            case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeURLObj:
                // res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseURLResponseModel is populated
            case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeFile:
                // res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseFileResponseModel is populated
            case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeText:
                // res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseTextResponseModel is populated
            case operations.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatchTypeFolder:
                // res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetKnowledgeBaseFolderResponseModel is populated
            default:
                // Unknown type - use res.ResponseUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                        | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      | Example                                                                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                            | :heavy_check_mark:                                                                                                                                               | The context to use for the request.                                                                                                                              |                                                                                                                                                                  |
| `documentationID`                                                                                                                                                | `string`                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The id of a document from the knowledge base. This is returned on document addition.                                                                             | 21m00Tcm4TlvDq8ikWAM                                                                                                                                             |
| `body`                                                                                                                                                           | [components.BodyUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch](../../models/components/bodyupdatedocumentv1convaiknowledgebasedocumentationidpatch.md) | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                       | optionalnullable.OptionalNullable[`string`]                                                                                                                      | :heavy_minus_sign:                                                                                                                                               | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.        |                                                                                                                                                                  |
| `opts`                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                         | :heavy_minus_sign:                                                                                                                                               | The options for this request.                                                                                                                                    |                                                                                                                                                                  |

### Response

**[*operations.UpdateDocumentRouteResponse](../../models/operations/updatedocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetRagIndexOverview

Provides total size and other information of RAG indexes used by knowledgebase documents

### Example Usage

<!-- UsageSnippet language="go" operationID="get_rag_index_overview" method="get" path="/v1/convai/knowledge-base/rag-index" -->
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

    res, err := s.AgentsPlatform.GetRagIndexOverview(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGIndexOverviewResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetRagIndexOverviewResponse](../../models/operations/getragindexoverviewresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetOrCreateRagIndexes

Retrieves and/or creates RAG indexes for multiple knowledge base documents in a single request. Maximum 100 items per request.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_or_create_rag_indexes" method="post" path="/v1/convai/knowledge-base/rag-index" -->
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

    res, err := s.AgentsPlatform.GetOrCreateRagIndexes(ctx, components.BodyComputeRAGIndexesInBatchV1ConvaiKnowledgeBaseRAGIndexPost{
        Items: []components.GetOrCreateRAGIndexRequestModel{
            components.GetOrCreateRAGIndexRequestModel{
                DocumentID: "<id>",
                CreateIfMissing: false,
            },
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseComputeRagIndexesInBatchV1ConvaiKnowledgeBaseRagIndexPost != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                            | Type                                                                                                                                                                 | Required                                                                                                                                                             | Description                                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                | :heavy_check_mark:                                                                                                                                                   | The context to use for the request.                                                                                                                                  |
| `body`                                                                                                                                                               | [components.BodyComputeRAGIndexesInBatchV1ConvaiKnowledgeBaseRAGIndexPost](../../models/components/bodycomputeragindexesinbatchv1convaiknowledgebaseragindexpost.md) | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `xiAPIKey`                                                                                                                                                           | optionalnullable.OptionalNullable[`string`]                                                                                                                          | :heavy_minus_sign:                                                                                                                                                   | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.            |
| `opts`                                                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                                                             | :heavy_minus_sign:                                                                                                                                                   | The options for this request.                                                                                                                                        |

### Response

**[*operations.GetOrCreateRagIndexesResponse](../../models/operations/getorcreateragindexesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RefreshURLDocumentRoute

Manually refresh a URL document by re-fetching its content from the source URL.

### Example Usage

<!-- UsageSnippet language="go" operationID="refresh_url_document_route" method="post" path="/v1/convai/knowledge-base/{documentation_id}/refresh" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.RefreshURLDocumentRoute(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost != nil {
        switch res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost.Type {
            case operations.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPostTypeURLObj:
                // res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost.GetKnowledgeBaseURLResponseModel is populated
            case operations.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPostTypeFile:
                // res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost.GetKnowledgeBaseFileResponseModel is populated
            case operations.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPostTypeText:
                // res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost.GetKnowledgeBaseTextResponseModel is populated
            case operations.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPostTypeFolder:
                // res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost.GetKnowledgeBaseFolderResponseModel is populated
            default:
                // Unknown type - use res.ResponseRefreshURLDocumentContentV1ConvaiKnowledgeBaseDocumentationIDRefreshPost.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.RefreshURLDocumentRouteResponse](../../models/operations/refreshurldocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetRagIndexes

Provides information about all RAG indexes of the specified knowledgebase document.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_rag_indexes" method="get" path="/v1/convai/knowledge-base/{documentation_id}/rag-index" -->
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

    res, err := s.AgentsPlatform.GetRagIndexes(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGDocumentIndexesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetRagIndexesResponse](../../models/operations/getragindexesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RagIndexStatus

In case the document is not RAG indexed, it triggers rag indexing task, otherwise it just returns the current status.

### Example Usage

<!-- UsageSnippet language="go" operationID="rag_index_status" method="post" path="/v1/convai/knowledge-base/{documentation_id}/rag-index" -->
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

    res, err := s.AgentsPlatform.RagIndexStatus(ctx, "21m00Tcm4TlvDq8ikWAM", components.RAGIndexRequestModel{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGDocumentIndexResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `body`                                                                                                                                                    | [components.RAGIndexRequestModel](../../models/components/ragindexrequestmodel.md)                                                                        | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.RagIndexStatusResponse](../../models/operations/ragindexstatusresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteRagIndex

Delete RAG index for the knowledgebase document.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_rag_index" method="delete" path="/v1/convai/knowledge-base/{documentation_id}/rag-index/{rag_index_id}" -->
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

    res, err := s.AgentsPlatform.DeleteRagIndex(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGDocumentIndexResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `ragIndexID`                                                                                                                                              | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of RAG index of document from the knowledge base.                                                                                                  | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeleteRagIndexResponse](../../models/operations/deleteragindexresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SearchKnowledgeBaseContentRoute

Fuzzy text search over knowledge base document content

### Example Usage

<!-- UsageSnippet language="go" operationID="search_knowledge_base_content_route" method="get" path="/v1/convai/knowledge-base/search" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.SearchKnowledgeBaseContentRoute(ctx, operations.SearchKnowledgeBaseContentRouteRequest{
        Query: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseContentSearchResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                              | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                  | :heavy_check_mark:                                                                                                     | The context to use for the request.                                                                                    |
| `request`                                                                                                              | [operations.SearchKnowledgeBaseContentRouteRequest](../../models/operations/searchknowledgebasecontentrouterequest.md) | :heavy_check_mark:                                                                                                     | The request object to use for the request.                                                                             |
| `opts`                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                               | :heavy_minus_sign:                                                                                                     | The options for this request.                                                                                          |

### Response

**[*operations.SearchKnowledgeBaseContentRouteResponse](../../models/operations/searchknowledgebasecontentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetKnowledgeBaseDependentAgents

Get a list of agents depending on this knowledge base document

### Example Usage

<!-- UsageSnippet language="go" operationID="get_knowledge_base_dependent_agents" method="get" path="/v1/convai/knowledge-base/{documentation_id}/dependent-agents" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetKnowledgeBaseDependentAgents(ctx, operations.GetKnowledgeBaseDependentAgentsRequest{
        DocumentationID: "21m00Tcm4TlvDq8ikWAM",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetKnowledgeBaseDependentAgentsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                              | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                  | :heavy_check_mark:                                                                                                     | The context to use for the request.                                                                                    |
| `request`                                                                                                              | [operations.GetKnowledgeBaseDependentAgentsRequest](../../models/operations/getknowledgebasedependentagentsrequest.md) | :heavy_check_mark:                                                                                                     | The request object to use for the request.                                                                             |
| `opts`                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                               | :heavy_minus_sign:                                                                                                     | The options for this request.                                                                                          |

### Response

**[*operations.GetKnowledgeBaseDependentAgentsResponse](../../models/operations/getknowledgebasedependentagentsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetKnowledgeBaseContent

Get the entire content of a document from the knowledge base

### Example Usage

<!-- UsageSnippet language="go" operationID="get_knowledge_base_content" method="get" path="/v1/convai/knowledge-base/{documentation_id}/content" -->
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

    res, err := s.AgentsPlatform.GetKnowledgeBaseContent(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetKnowledgeBaseContentResponse](../../models/operations/getknowledgebasecontentresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetKnowledgeBaseSourceFileURL

Get a signed URL to download the original source file of a file-type document from the knowledge base

### Example Usage

<!-- UsageSnippet language="go" operationID="get_knowledge_base_source_file_url" method="get" path="/v1/convai/knowledge-base/{documentation_id}/source-file-url" -->
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

    res, err := s.AgentsPlatform.GetKnowledgeBaseSourceFileURL(ctx, "21m00Tcm4TlvDq8ikWAM", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseSourceFileURLResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetKnowledgeBaseSourceFileURLResponse](../../models/operations/getknowledgebasesourcefileurlresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetDocumentationChunkFromKnowledgeBase

Get details about a specific documentation part used by RAG.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_documentation_chunk_from_knowledge_base" method="get" path="/v1/convai/knowledge-base/{documentation_id}/chunk/{chunk_id}" -->
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

    res, err := s.AgentsPlatform.GetDocumentationChunkFromKnowledgeBase(ctx, "21m00Tcm4TlvDq8ikWAM", "1", optionalnullable.From(elevenlabsgo.Pointer(components.EmbeddingModelEnumE5Mistral7bInstruct)), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseDocumentChunkResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `documentationID`                                                                                                                                         | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document from the knowledge base. This is returned on document addition.                                                                      | 21m00Tcm4TlvDq8ikWAM                                                                                                                                      |
| `chunkID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of a document RAG chunk from the knowledge base.                                                                                                   | 1                                                                                                                                                         |
| `embeddingModel`                                                                                                                                          | optionalnullable.OptionalNullable[[components.EmbeddingModelEnum](../../models/components/embeddingmodelenum.md)]                                         | :heavy_minus_sign:                                                                                                                                        | The embedding model used to retrieve the chunk.                                                                                                           |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetDocumentationChunkFromKnowledgeBaseResponse](../../models/operations/getdocumentationchunkfromknowledgebaseresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetToolsRoute

Get all available tools in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_tools_route" method="get" path="/v1/convai/tools" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetToolsRoute(ctx, operations.GetToolsRouteRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.ToolsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                          | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `ctx`                                                                              | [context.Context](https://pkg.go.dev/context#Context)                              | :heavy_check_mark:                                                                 | The context to use for the request.                                                |
| `request`                                                                          | [operations.GetToolsRouteRequest](../../models/operations/gettoolsrouterequest.md) | :heavy_check_mark:                                                                 | The request object to use for the request.                                         |
| `opts`                                                                             | [][operations.Option](../../models/operations/option.md)                           | :heavy_minus_sign:                                                                 | The options for this request.                                                      |

### Response

**[*operations.GetToolsRouteResponse](../../models/operations/gettoolsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddToolRoute

Add a new tool to the available tools in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_tool_route" method="post" path="/v1/convai/tools" -->
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

    res, err := s.AgentsPlatform.AddToolRoute(ctx, components.ToolRequestModel{
        ToolConfig: components.CreateToolRequestModelToolConfigClient(
            components.ClientToolConfigInput{
                Name: "<value>",
                Description: "meh smuggle athwart yahoo whoa rapid interestingly ugh",
            },
        ),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ToolResponseModel != nil {
        switch res.ToolResponseModel.ToolConfig.Type {
            case components.ToolResponseModelToolConfigTypeClient:
                // res.ToolResponseModel.ToolConfig.ClientToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeMcp:
                // res.ToolResponseModel.ToolConfig.MCPToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeSystem:
                // res.ToolResponseModel.ToolConfig.SystemToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeWebhook:
                // res.ToolResponseModel.ToolConfig.WebhookToolConfigOutput is populated
            default:
                // Unknown type - use res.ToolResponseModel.ToolConfig.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.ToolRequestModel](../../models/components/toolrequestmodel.md)                                                                                | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.AddToolRouteResponse](../../models/operations/addtoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetToolRoute

Get tool that is available in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_tool_route" method="get" path="/v1/convai/tools/{tool_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/components"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetToolRoute(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ToolResponseModel != nil {
        switch res.ToolResponseModel.ToolConfig.Type {
            case components.ToolResponseModelToolConfigTypeClient:
                // res.ToolResponseModel.ToolConfig.ClientToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeMcp:
                // res.ToolResponseModel.ToolConfig.MCPToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeSystem:
                // res.ToolResponseModel.ToolConfig.SystemToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeWebhook:
                // res.ToolResponseModel.ToolConfig.WebhookToolConfigOutput is populated
            default:
                // Unknown type - use res.ToolResponseModel.ToolConfig.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `toolID`                                                                                                                                                  | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the requested tool.                                                                                                                                 |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetToolRouteResponse](../../models/operations/gettoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteToolRoute

Delete tool from the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_tool_route" method="delete" path="/v1/convai/tools/{tool_id}" -->
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

    res, err := s.AgentsPlatform.DeleteToolRoute(ctx, "<id>", elevenlabsgo.Pointer(false), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `toolID`                                                                                                                                                  | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the requested tool.                                                                                                                                 |
| `force`                                                                                                                                                   | `*bool`                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                        | If set to true, the tool will be deleted regardless of whether it is used by any agents and it will be removed from the dependent agents and branches.    |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteToolRouteResponse](../../models/operations/deletetoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateToolRoute

Update tool that is available in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_tool_route" method="patch" path="/v1/convai/tools/{tool_id}" -->
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

    res, err := s.AgentsPlatform.UpdateToolRoute(ctx, "<id>", components.ToolRequestModel{
        ToolConfig: components.CreateToolRequestModelToolConfigClient(
            components.ClientToolConfigInput{
                Name: "<value>",
                Description: "oh well-lit but underneath against uh-huh rationalise quicker",
            },
        ),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ToolResponseModel != nil {
        switch res.ToolResponseModel.ToolConfig.Type {
            case components.ToolResponseModelToolConfigTypeClient:
                // res.ToolResponseModel.ToolConfig.ClientToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeMcp:
                // res.ToolResponseModel.ToolConfig.MCPToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeSystem:
                // res.ToolResponseModel.ToolConfig.SystemToolConfigOutput is populated
            case components.ToolResponseModelToolConfigTypeWebhook:
                // res.ToolResponseModel.ToolConfig.WebhookToolConfigOutput is populated
            default:
                // Unknown type - use res.ToolResponseModel.ToolConfig.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `toolID`                                                                                                                                                  | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the requested tool.                                                                                                                                 |
| `body`                                                                                                                                                    | [components.ToolRequestModel](../../models/components/toolrequestmodel.md)                                                                                | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateToolRouteResponse](../../models/operations/updatetoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetToolDependentAgentsRoute

Get a list of agents depending on this tool

### Example Usage

<!-- UsageSnippet language="go" operationID="get_tool_dependent_agents_route" method="get" path="/v1/convai/tools/{tool_id}/dependent-agents" -->
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

    res, err := s.AgentsPlatform.GetToolDependentAgentsRoute(ctx, "<id>", optionalnullable.From[string](nil), elevenlabsgo.Pointer[int64](30), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetToolDependentAgentsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `toolID`                                                                                                                                                  | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the requested tool.                                                                                                                                 |
| `cursor`                                                                                                                                                  | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Used for fetching next page. Cursor is returned in the response.                                                                                          |
| `pageSize`                                                                                                                                                | `*int64`                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                        | How many documents to return at maximum. Can not exceed 100, defaults to 30.                                                                              |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetToolDependentAgentsRouteResponse](../../models/operations/gettooldependentagentsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSettingsRoute

Retrieve Convai settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_settings_route" method="get" path="/v1/convai/settings" -->
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

    res, err := s.AgentsPlatform.GetSettingsRoute(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAISettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetSettingsRouteResponse](../../models/operations/getsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSettingsRoute

Update Convai settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="update_settings_route" method="patch" path="/v1/convai/settings" -->
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

    res, err := s.AgentsPlatform.UpdateSettingsRoute(ctx, components.PatchConvAISettingsRequest{
        ConversationInitiationClientDataWebhook: optionalnullable.From(&components.ConversationInitiationClientDataWebhook{
            URL: "https://example.com/webhook",
            RequestHeaders: map[string]components.ConversationInitiationClientDataWebhookRequestHeaders{
                "Content-Type": components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(
                    "application/json",
                ),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAISettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.PatchConvAISettingsRequest](../../models/components/patchconvaisettingsrequest.md)                                                            | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateSettingsRouteResponse](../../models/operations/updatesettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetDashboardSettingsRoute

Retrieve Convai dashboard settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_dashboard_settings_route" method="get" path="/v1/convai/settings/dashboard" -->
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

    res, err := s.AgentsPlatform.GetDashboardSettingsRoute(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAIDashboardSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetDashboardSettingsRouteResponse](../../models/operations/getdashboardsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateDashboardSettingsRoute

Update Convai dashboard settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="update_dashboard_settings_route" method="patch" path="/v1/convai/settings/dashboard" -->
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

    res, err := s.AgentsPlatform.UpdateDashboardSettingsRoute(ctx, components.PatchConvAIDashboardSettingsRequest{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAIDashboardSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.PatchConvAIDashboardSettingsRequest](../../models/components/patchconvaidashboardsettingsrequest.md)                                          | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateDashboardSettingsRouteResponse](../../models/operations/updatedashboardsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSecretsRoute

Get all workspace secrets for the user

### Example Usage

<!-- UsageSnippet language="go" operationID="get_secrets_route" method="get" path="/v1/convai/secrets" -->
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

    res, err := s.AgentsPlatform.GetSecretsRoute(ctx, optionalnullable.From[int64](nil), optionalnullable.From[string](nil), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetWorkspaceSecretsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `pageSize`                                                                                                                                                | optionalnullable.OptionalNullable[`int64`]                                                                                                                | :heavy_minus_sign:                                                                                                                                        | How many documents to return at maximum. Can not exceed 100. If not provided, returns all secrets.                                                        |
| `cursor`                                                                                                                                                  | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Used for fetching next page. Cursor is returned in the response.                                                                                          |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetSecretsRouteResponse](../../models/operations/getsecretsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateSecretRoute

Create a new secret for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="create_secret_route" method="post" path="/v1/convai/secrets" -->
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

    res, err := s.AgentsPlatform.CreateSecretRoute(ctx, components.PostWorkspaceSecretRequest{
        Name: "<value>",
        Value: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.PostWorkspaceSecretResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.PostWorkspaceSecretRequest](../../models/components/postworkspacesecretrequest.md)                                                            | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateSecretRouteResponse](../../models/operations/createsecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteSecretRoute

Delete a workspace secret if it's not in use

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_secret_route" method="delete" path="/v1/convai/secrets/{secret_id}" -->
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

    res, err := s.AgentsPlatform.DeleteSecretRoute(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `secretID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteSecretRouteResponse](../../models/operations/deletesecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSecretRoute

Update an existing secret for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="update_secret_route" method="patch" path="/v1/convai/secrets/{secret_id}" -->
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

    res, err := s.AgentsPlatform.UpdateSecretRoute(ctx, "<id>", components.PatchWorkspaceSecretRequest{
        Name: "<value>",
        Value: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.PostWorkspaceSecretResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `secretID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `body`                                                                                                                                                    | [components.PatchWorkspaceSecretRequest](../../models/components/patchworkspacesecretrequest.md)                                                          | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateSecretRouteResponse](../../models/operations/updatesecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateBatchCall

Submit a batch call request to schedule calls for multiple recipients.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_batch_call" method="post" path="/v1/convai/batch-calling/submit" -->
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

    res, err := s.AgentsPlatform.CreateBatchCall(ctx, components.BodySubmitABatchCallRequestV1ConvaiBatchCallingSubmitPost{
        CallName: "<value>",
        AgentID: "<id>",
        Recipients: []components.OutboundCallRecipient{},
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                    | Type                                                                                                                                                         | Required                                                                                                                                                     | Description                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                        | :heavy_check_mark:                                                                                                                                           | The context to use for the request.                                                                                                                          |
| `body`                                                                                                                                                       | [components.BodySubmitABatchCallRequestV1ConvaiBatchCallingSubmitPost](../../models/components/bodysubmitabatchcallrequestv1convaibatchcallingsubmitpost.md) | :heavy_check_mark:                                                                                                                                           | N/A                                                                                                                                                          |
| `xiAPIKey`                                                                                                                                                   | optionalnullable.OptionalNullable[`string`]                                                                                                                  | :heavy_minus_sign:                                                                                                                                           | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.    |
| `opts`                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                     | :heavy_minus_sign:                                                                                                                                           | The options for this request.                                                                                                                                |

### Response

**[*operations.CreateBatchCallResponse](../../models/operations/createbatchcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetWorkspaceBatchCalls

Get all batch calls for the current workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_workspace_batch_calls" method="get" path="/v1/convai/batch-calling/workspace" -->
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

    res, err := s.AgentsPlatform.GetWorkspaceBatchCalls(ctx, elevenlabsgo.Pointer[int64](100), optionalnullable.From[string](nil), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceBatchCallsResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `limit`                                                                                                                                                   | `*int64`                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |
| `lastDoc`                                                                                                                                                 | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetWorkspaceBatchCallsResponse](../../models/operations/getworkspacebatchcallsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetBatchCall

Get detailed information about a batch call including all recipients.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_batch_call" method="get" path="/v1/convai/batch-calling/{batch_id}" -->
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

    res, err := s.AgentsPlatform.GetBatchCall(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallDetailedResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `batchID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetBatchCallResponse](../../models/operations/getbatchcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteBatchCall

Permanently delete a batch call and all recipient records. Conversations remain in history.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_batch_call" method="delete" path="/v1/convai/batch-calling/{batch_id}" -->
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

    res, err := s.AgentsPlatform.DeleteBatchCall(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `batchID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteBatchCallResponse](../../models/operations/deletebatchcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CancelBatchCall

Cancel a running batch call and set all recipients to cancelled status.

### Example Usage

<!-- UsageSnippet language="go" operationID="cancel_batch_call" method="post" path="/v1/convai/batch-calling/{batch_id}/cancel" -->
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

    res, err := s.AgentsPlatform.CancelBatchCall(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `batchID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CancelBatchCallResponse](../../models/operations/cancelbatchcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RetryBatchCall

Retry a batch call, calling failed and no-response recipients again.

### Example Usage

<!-- UsageSnippet language="go" operationID="retry_batch_call" method="post" path="/v1/convai/batch-calling/{batch_id}/retry" -->
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

    res, err := s.AgentsPlatform.RetryBatchCall(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `batchID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.RetryBatchCallResponse](../../models/operations/retrybatchcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## HandleSipTrunkOutboundCall

Handle an outbound call via SIP trunk

### Example Usage

<!-- UsageSnippet language="go" operationID="handle_sip_trunk_outbound_call" method="post" path="/v1/convai/sip-trunk/outbound-call" -->
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

    res, err := s.AgentsPlatform.HandleSipTrunkOutboundCall(ctx, components.BodyHandleAnOutboundCallViaSIPTrunkV1ConvaiSIPTrunkOutboundCallPost{
        AgentID: "<id>",
        AgentPhoneNumberID: "<id>",
        ToNumber: "<value>",
        ConversationInitiationClientData: optionalnullable.From(&components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Turn: optionalnullable.From(&components.TurnConfigOverride{
                    SoftTimeoutConfig: optionalnullable.From(&components.SoftTimeoutConfigOverride{
                        Message: optionalnullable.From(elevenlabsgo.Pointer("Hhmmmm...yeah.")),
                    }),
                }),
                Tts: optionalnullable.From(&components.TTSConversationalConfigOverride{
                    VoiceID: optionalnullable.From(elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal")),
                    Stability: optionalnullable.From(elevenlabsgo.Pointer[float64](0.5)),
                    Speed: optionalnullable.From(elevenlabsgo.Pointer[float64](1.0)),
                    SimilarityBoost: optionalnullable.From(elevenlabsgo.Pointer[float64](0.8)),
                }),
                Agent: optionalnullable.From(&components.AgentConfigOverrideInput{
                    FirstMessage: optionalnullable.From(elevenlabsgo.Pointer("Hello, how can I help you today?")),
                    Language: optionalnullable.From(elevenlabsgo.Pointer("en")),
                    Prompt: optionalnullable.From(&components.PromptAgentAPIModelOverrideInput{
                        Prompt: optionalnullable.From(elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation.")),
                        Llm: optionalnullable.From(elevenlabsgo.Pointer(components.LlmGemini20Flash001)),
                        ToolIds: optionalnullable.From(elevenlabsgo.Pointer([]string{})),
                        KnowledgeBase: optionalnullable.From(elevenlabsgo.Pointer([]components.KnowledgeBaseLocator{})),
                    }),
                }),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.SIPTrunkOutboundCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                        | Type                                                                                                                                                                             | Required                                                                                                                                                                         | Description                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                            | :heavy_check_mark:                                                                                                                                                               | The context to use for the request.                                                                                                                                              |
| `body`                                                                                                                                                                           | [components.BodyHandleAnOutboundCallViaSIPTrunkV1ConvaiSIPTrunkOutboundCallPost](../../models/components/bodyhandleanoutboundcallviasiptrunkv1convaisiptrunkoutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                               | N/A                                                                                                                                                                              |
| `xiAPIKey`                                                                                                                                                                       | optionalnullable.OptionalNullable[`string`]                                                                                                                                      | :heavy_minus_sign:                                                                                                                                                               | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                        |
| `opts`                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                         | :heavy_minus_sign:                                                                                                                                                               | The options for this request.                                                                                                                                                    |

### Response

**[*operations.HandleSipTrunkOutboundCallResponse](../../models/operations/handlesiptrunkoutboundcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListMcpServersRoute

Retrieve all MCP server configurations available in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_mcp_servers_route" method="get" path="/v1/convai/mcp-servers" -->
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

    res, err := s.AgentsPlatform.ListMcpServersRoute(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServersResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.ListMcpServersRouteResponse](../../models/operations/listmcpserversrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateMcpServerRoute

Create a new MCP server configuration in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_mcp_server_route" method="post" path="/v1/convai/mcp-servers" -->
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

    res, err := s.AgentsPlatform.CreateMcpServerRoute(ctx, components.MCPServerRequestModel{
        Config: components.MCPServerConfigInput{
            URL: components.CreateMCPServerConfigInputURLStr(
                "https://babyish-injunction.info",
            ),
            Name: "<value>",
            ToolConfigOverrides: []components.MCPToolConfigOverride{
                components.MCPToolConfigOverride{
                    ToolName: "<value>",
                    Assignments: []components.DynamicVariableAssignment{
                        components.DynamicVariableAssignment{
                            DynamicVariable: "user_name",
                            ValuePath: "user.name",
                        },
                    },
                },
            },
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [components.MCPServerRequestModel](../../models/components/mcpserverrequestmodel.md)                                                                      | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateMcpServerRouteResponse](../../models/operations/createmcpserverrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetMcpRoute

Retrieve a specific MCP server configuration from the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_mcp_route" method="get" path="/v1/convai/mcp-servers/{mcp_server_id}" -->
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

    res, err := s.AgentsPlatform.GetMcpRoute(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetMcpRouteResponse](../../models/operations/getmcprouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteMcpServerRoute

Delete a specific MCP server configuration from the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_mcp_server_route" method="delete" path="/v1/convai/mcp-servers/{mcp_server_id}" -->
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

    res, err := s.AgentsPlatform.DeleteMcpServerRoute(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteMcpServerRouteResponse](../../models/operations/deletemcpserverrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateMcpServerConfigRoute

Update the configuration settings for an MCP server.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_mcp_server_config_route" method="patch" path="/v1/convai/mcp-servers/{mcp_server_id}" -->
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

    res, err := s.AgentsPlatform.UpdateMcpServerConfigRoute(ctx, "<id>", components.MCPServerConfigUpdateRequestModel{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `body`                                                                                                                                                    | [components.MCPServerConfigUpdateRequestModel](../../models/components/mcpserverconfigupdaterequestmodel.md)                                              | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateMcpServerConfigRouteResponse](../../models/operations/updatemcpserverconfigrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListMcpServerToolsRoute

Retrieve all tools available for a specific MCP server configuration.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_mcp_server_tools_route" method="get" path="/v1/convai/mcp-servers/{mcp_server_id}/tools" -->
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

    res, err := s.AgentsPlatform.ListMcpServerToolsRoute(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ListMCPToolsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.ListMcpServerToolsRouteResponse](../../models/operations/listmcpservertoolsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ~~UpdateMcpServerApprovalPolicyRoute~~

Update the approval policy configuration for an MCP server. DEPRECATED: Use PATCH /mcp-servers/{id} endpoint instead.

> :warning: **DEPRECATED**: This will be removed in a future release, please migrate away from it as soon as possible.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_mcp_server_approval_policy_route" method="patch" path="/v1/convai/mcp-servers/{mcp_server_id}/approval-policy" -->
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

    res, err := s.AgentsPlatform.UpdateMcpServerApprovalPolicyRoute(ctx, "<id>", components.MCPApprovalPolicyUpdateRequestModel{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `body`                                                                                                                                                    | [components.MCPApprovalPolicyUpdateRequestModel](../../models/components/mcpapprovalpolicyupdaterequestmodel.md)                                          | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateMcpServerApprovalPolicyRouteResponse](../../models/operations/updatemcpserverapprovalpolicyrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddMcpServerToolApprovalRoute

Add approval for a specific MCP tool when using per-tool approval mode.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_mcp_server_tool_approval_route" method="post" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-approvals" -->
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

    res, err := s.AgentsPlatform.AddMcpServerToolApprovalRoute(ctx, "<id>", components.MCPToolAddApprovalRequestModel{
        ToolName: "<value>",
        ToolDescription: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `body`                                                                                                                                                    | [components.MCPToolAddApprovalRequestModel](../../models/components/mcptooladdapprovalrequestmodel.md)                                                    | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.AddMcpServerToolApprovalRouteResponse](../../models/operations/addmcpservertoolapprovalrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RemoveMcpServerToolApprovalRoute

Remove approval for a specific MCP tool when using per-tool approval mode.

### Example Usage

<!-- UsageSnippet language="go" operationID="remove_mcp_server_tool_approval_route" method="delete" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-approvals/{tool_name}" -->
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

    res, err := s.AgentsPlatform.RemoveMcpServerToolApprovalRoute(ctx, "<id>", "<value>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `toolName`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Name of the MCP tool to remove approval for.                                                                                                              |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.RemoveMcpServerToolApprovalRouteResponse](../../models/operations/removemcpservertoolapprovalrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddMcpToolConfigOverrideRoute

Create configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_mcp_tool_config_override_route" method="post" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs" -->
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

    res, err := s.AgentsPlatform.AddMcpToolConfigOverrideRoute(ctx, "<id>", components.MCPToolConfigOverrideCreateRequestModel{
        Assignments: optionalnullable.From(elevenlabsgo.Pointer([]components.DynamicVariableAssignment{
            components.DynamicVariableAssignment{
                DynamicVariable: "user_name",
                ValuePath: "user.name",
            },
        })),
        ToolName: "<value>",
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `body`                                                                                                                                                    | [components.MCPToolConfigOverrideCreateRequestModel](../../models/components/mcptoolconfigoverridecreaterequestmodel.md)                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.AddMcpToolConfigOverrideRouteResponse](../../models/operations/addmcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetMcpToolConfigOverrideRoute

Retrieve configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_mcp_tool_config_override_route" method="get" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs/{tool_name}" -->
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

    res, err := s.AgentsPlatform.GetMcpToolConfigOverrideRoute(ctx, "<id>", "<value>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPToolConfigOverride != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `toolName`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Name of the MCP tool to retrieve config overrides for.                                                                                                    |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetMcpToolConfigOverrideRouteResponse](../../models/operations/getmcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RemoveMcpToolConfigOverrideRoute

Remove configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="remove_mcp_tool_config_override_route" method="delete" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs/{tool_name}" -->
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

    res, err := s.AgentsPlatform.RemoveMcpToolConfigOverrideRoute(ctx, "<id>", "<value>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `toolName`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Name of the MCP tool to remove config overrides for.                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.RemoveMcpToolConfigOverrideRouteResponse](../../models/operations/removemcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateMcpToolConfigOverrideRoute

Update configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_mcp_tool_config_override_route" method="patch" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs/{tool_name}" -->
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

    res, err := s.AgentsPlatform.UpdateMcpToolConfigOverrideRoute(ctx, "<id>", "<value>", components.MCPToolConfigOverrideUpdateRequestModel{
        Assignments: optionalnullable.From(elevenlabsgo.Pointer([]components.DynamicVariableAssignment{
            components.DynamicVariableAssignment{
                DynamicVariable: "user_name",
                ValuePath: "user.name",
            },
        })),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `mcpServerID`                                                                                                                                             | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | ID of the MCP Server.                                                                                                                                     |
| `toolName`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Name of the MCP tool to update config overrides for.                                                                                                      |
| `body`                                                                                                                                                    | [components.MCPToolConfigOverrideUpdateRequestModel](../../models/components/mcptoolconfigoverrideupdaterequestmodel.md)                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateMcpToolConfigOverrideRouteResponse](../../models/operations/updatemcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetWhatsappAccount

Get a WhatsApp account

### Example Usage

<!-- UsageSnippet language="go" operationID="get_whatsapp_account" method="get" path="/v1/convai/whatsapp-accounts/{phone_number_id}" -->
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

    res, err := s.AgentsPlatform.GetWhatsappAccount(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetWhatsAppAccountResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `phoneNumberID`                                                                                                                                           | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetWhatsappAccountResponse](../../models/operations/getwhatsappaccountresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteWhatsappAccount

Delete a WhatsApp account

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_whatsapp_account" method="delete" path="/v1/convai/whatsapp-accounts/{phone_number_id}" -->
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

    res, err := s.AgentsPlatform.DeleteWhatsappAccount(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `phoneNumberID`                                                                                                                                           | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.DeleteWhatsappAccountResponse](../../models/operations/deletewhatsappaccountresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateWhatsappAccount

Update a WhatsApp account

### Example Usage

<!-- UsageSnippet language="go" operationID="update_whatsapp_account" method="patch" path="/v1/convai/whatsapp-accounts/{phone_number_id}" -->
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

    res, err := s.AgentsPlatform.UpdateWhatsappAccount(ctx, "<id>", components.UpdateWhatsAppAccountRequest{}, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `phoneNumberID`                                                                                                                                           | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `body`                                                                                                                                                    | [components.UpdateWhatsAppAccountRequest](../../models/components/updatewhatsappaccountrequest.md)                                                        | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateWhatsappAccountResponse](../../models/operations/updatewhatsappaccountresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListWhatsappAccounts

List all WhatsApp accounts

### Example Usage

<!-- UsageSnippet language="go" operationID="list_whatsapp_accounts" method="get" path="/v1/convai/whatsapp-accounts" -->
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

    res, err := s.AgentsPlatform.ListWhatsappAccounts(ctx, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ListWhatsAppAccountsResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.ListWhatsappAccountsResponse](../../models/operations/listwhatsappaccountsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetBranchesRoute

Returns a list of branches an agent has

### Example Usage

<!-- UsageSnippet language="go" operationID="get_branches_route" method="get" path="/v1/convai/agents/{agent_id}/branches" -->
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

    res, err := s.AgentsPlatform.GetBranchesRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", elevenlabsgo.Pointer(false), elevenlabsgo.Pointer[int64](100), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.ListResponseAgentBranchSummary != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `includeArchived`                                                                                                                                         | `*bool`                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                        | Whether archived branches should be included                                                                                                              |                                                                                                                                                           |
| `limit`                                                                                                                                                   | `*int64`                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                        | How many results at most should be returned                                                                                                               |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetBranchesRouteResponse](../../models/operations/getbranchesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateBranchRoute

Create a new branch from a given version of any branch

### Example Usage

<!-- UsageSnippet language="go" operationID="create_branch_route" method="post" path="/v1/convai/agents/{agent_id}/branches" -->
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

    res, err := s.AgentsPlatform.CreateBranchRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodyCreateANewBranchV1ConvaiAgentsAgentIDBranchesPost{
        ParentVersionID: "<id>",
        Name: "<value>",
        Description: "faithfully platter equally red",
        Workflow: optionalnullable.From(&components.AgentWorkflowRequestModel{
            Edges: map[string]components.WorkflowEdgeModelInput{
                "entry_to_tool_a": components.WorkflowEdgeModelInput{
                    Source: "entry_node",
                    Target: "tool_node_a",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: true,
                        },
                    ))),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputAndOperator(
                                components.ASTAndOperatorNodeInput1{
                                    Children: []components.ASTNodeInput{},
                                },
                            ),
                        },
                    ))),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputLlm(
                                components.CreateASTLLMNodeInputASTLLMNode2(
                                    components.ASTLLMNode2{
                                        Prompt: "<value>",
                                    },
                                ),
                            ),
                        },
                    ))),
                },
            },
            Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                "entry_node": components.CreateAgentWorkflowRequestModelNodesStart(
                    components.WorkflowStartNodeModelInput{},
                ),
                "failure_node": components.CreateAgentWorkflowRequestModelNodesTool(
                    components.WorkflowToolNodeModelInput{},
                ),
                "start_node": components.CreateAgentWorkflowRequestModelNodesStart(
                    components.WorkflowStartNodeModelInput{},
                ),
                "success_conversation": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                    components.WorkflowOverrideAgentNodeModelInput{
                        Label: "<value>",
                    },
                ),
                "success_end": components.CreateAgentWorkflowRequestModelNodesTool(
                    components.WorkflowToolNodeModelInput{},
                ),
                "success_phone": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                    components.WorkflowPhoneNumberNodeModelInput{
                        TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationPhone(
                            components.PhoneNumberTransferDestination{
                                PhoneNumber: "544-466-1777 x747",
                            },
                        ),
                    },
                ),
                "success_transfer": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: "<id>",
                    },
                ),
                "tool_node_a": components.CreateAgentWorkflowRequestModelNodesStart(
                    components.WorkflowStartNodeModelInput{},
                ),
                "tool_node_b": components.CreateAgentWorkflowRequestModelNodesTool(
                    components.WorkflowToolNodeModelInput{},
                ),
            },
        }),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentBranchResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `body`                                                                                                                                                    | [components.BodyCreateANewBranchV1ConvaiAgentsAgentIDBranchesPost](../../models/components/bodycreateanewbranchv1convaiagentsagentidbranchespost.md)      | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.CreateBranchRouteResponse](../../models/operations/createbranchrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetBranchRoute

Get information about a single agent branch

### Example Usage

<!-- UsageSnippet language="go" operationID="get_branch_route" method="get" path="/v1/convai/agents/{agent_id}/branches/{branch_id}" -->
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

    res, err := s.AgentsPlatform.GetBranchRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbranch_0901k4aafjxxfxt93gd841r7tv5t", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AgentBranchResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `branchID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Unique identifier for the branch.                                                                                                                         | agtbranch_0901k4aafjxxfxt93gd841r7tv5t                                                                                                                    |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.GetBranchRouteResponse](../../models/operations/getbranchrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateBranchRoute

Update agent branch properties such as archiving status and protection level

### Example Usage

<!-- UsageSnippet language="go" operationID="update_branch_route" method="patch" path="/v1/convai/agents/{agent_id}/branches/{branch_id}" -->
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

    res, err := s.AgentsPlatform.UpdateBranchRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbranch_0901k4aafjxxfxt93gd841r7tv5t", optionalnullable.From[string](nil), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.AgentBranchResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                 | Type                                                                                                                                                                      | Required                                                                                                                                                                  | Description                                                                                                                                                               | Example                                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                     | :heavy_check_mark:                                                                                                                                                        | The context to use for the request.                                                                                                                                       |                                                                                                                                                                           |
| `agentID`                                                                                                                                                                 | `string`                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                                        |
| `branchID`                                                                                                                                                                | `string`                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                        | Unique identifier for the branch.                                                                                                                                         | agtbranch_0901k4aafjxxfxt93gd841r7tv5t                                                                                                                                    |
| `xiAPIKey`                                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                                               | :heavy_minus_sign:                                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                 |                                                                                                                                                                           |
| `body`                                                                                                                                                                    | [*components.BodyUpdateAgentBranchV1ConvaiAgentsAgentIDBranchesBranchIDPatch](../../models/components/bodyupdateagentbranchv1convaiagentsagentidbranchesbranchidpatch.md) | :heavy_minus_sign:                                                                                                                                                        | N/A                                                                                                                                                                       |                                                                                                                                                                           |
| `opts`                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                  | :heavy_minus_sign:                                                                                                                                                        | The options for this request.                                                                                                                                             |                                                                                                                                                                           |

### Response

**[*operations.UpdateBranchRouteResponse](../../models/operations/updatebranchrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## MergeBranchIntoTarget

Merge a branch into a target branch

### Example Usage

<!-- UsageSnippet language="go" operationID="merge_branch_into_target" method="post" path="/v1/convai/agents/{agent_id}/branches/{source_branch_id}/merge" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.MergeBranchIntoTarget(ctx, operations.MergeBranchIntoTargetRequest{
        AgentID: "agent_3701k3ttaq12ewp8b7qv5rfyszkz",
        SourceBranchID: "agtbrch_8901k4t9z5defmb8vh3e9361y7nj",
        TargetBranchID: "agtbrch_8901k4t9z5defmb8vh3e9361y7nj",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                          | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                              | :heavy_check_mark:                                                                                 | The context to use for the request.                                                                |
| `request`                                                                                          | [operations.MergeBranchIntoTargetRequest](../../models/operations/mergebranchintotargetrequest.md) | :heavy_check_mark:                                                                                 | The request object to use for the request.                                                         |
| `opts`                                                                                             | [][operations.Option](../../models/operations/option.md)                                           | :heavy_minus_sign:                                                                                 | The options for this request.                                                                      |

### Response

**[*operations.MergeBranchIntoTargetResponse](../../models/operations/mergebranchintotargetresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentDeploymentRoute

Create a new deployment for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_deployment_route" method="post" path="/v1/convai/agents/{agent_id}/deployments" -->
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

    res, err := s.AgentsPlatform.CreateAgentDeploymentRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodyCreateOrUpdateDeploymentsV1ConvaiAgentsAgentIDDeploymentsPost{
        DeploymentRequest: components.AgentDeploymentRequest{
            Requests: []components.AgentDeploymentRequestItem{
                components.AgentDeploymentRequestItem{
                    BranchID: "agtbrch_8901k4t9z5defmb8vh3e9361y7nj",
                    DeploymentStrategy: components.AgentDeploymentPercentageStrategy{
                        TrafficPercentage: 0.5,
                    },
                },
            },
        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.AgentDeploymentResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                    | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  | Example                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                        | :heavy_check_mark:                                                                                                                                                           | The context to use for the request.                                                                                                                                          |                                                                                                                                                                              |
| `agentID`                                                                                                                                                                    | `string`                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | The id of an agent. This is returned on agent creation.                                                                                                                      | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                                           |
| `body`                                                                                                                                                                       | [components.BodyCreateOrUpdateDeploymentsV1ConvaiAgentsAgentIDDeploymentsPost](../../models/components/bodycreateorupdatedeploymentsv1convaiagentsagentiddeploymentspost.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |                                                                                                                                                                              |
| `xiAPIKey`                                                                                                                                                                   | optionalnullable.OptionalNullable[`string`]                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                           | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website.                    |                                                                                                                                                                              |
| `opts`                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | The options for this request.                                                                                                                                                |                                                                                                                                                                              |

### Response

**[*operations.CreateAgentDeploymentRouteResponse](../../models/operations/createagentdeploymentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentDraftRoute

Create a new draft for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_draft_route" method="post" path="/v1/convai/agents/{agent_id}/drafts" -->
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

    res, err := s.AgentsPlatform.CreateAgentDraftRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", components.BodyCreateAgentDraftV1ConvaiAgentsAgentIDDraftsPost{
        ConversationConfig: map[string]any{
            "key": "<value>",
            "key1": "<value>",
        },
        PlatformSettings: map[string]any{

        },
        Workflow: components.AgentWorkflowRequestModel{
            Edges: map[string]components.WorkflowEdgeModelInput{
                "entry_to_tool_a": components.WorkflowEdgeModelInput{
                    Source: "entry_node",
                    Target: "tool_node_a",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputStringLiteral(
                                components.ASTStringNodeInput{
                                    Value: "<value>",
                                },
                            ),
                        },
                    ))),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    ))),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    ))),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: optionalnullable.From(elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: false,
                        },
                    ))),
                },
            },
            Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                "entry_node": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
                "failure_node": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: "<id>",
                    },
                ),
                "start_node": components.CreateAgentWorkflowRequestModelNodesStart(
                    components.WorkflowStartNodeModelInput{},
                ),
                "success_conversation": components.CreateAgentWorkflowRequestModelNodesPhoneNumber(
                    components.WorkflowPhoneNumberNodeModelInput{
                        TransferDestination: components.CreateWorkflowPhoneNumberNodeModelInputTransferDestinationSipURIDynamicVariable(
                            components.SIPURIDynamicVariableTransferDestination{
                                SipURI: "https://emotional-brook.org/",
                            },
                        ),
                    },
                ),
                "success_end": components.CreateAgentWorkflowRequestModelNodesOverrideAgent(
                    components.WorkflowOverrideAgentNodeModelInput{
                        Label: "<value>",
                    },
                ),
                "success_phone": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: "<id>",
                    },
                ),
                "success_transfer": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: "<id>",
                    },
                ),
                "tool_node_a": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
                "tool_node_b": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
            },
        },
        Name: "<value>",
        Tags: optionalnullable.From(elevenlabsgo.Pointer([]string{
            "Customer Support",
            "Technical Help",
            "Eleven",
        })),
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `branchID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The ID of the agent branch to use                                                                                                                         | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                                                                                                      |
| `body`                                                                                                                                                    | [components.BodyCreateAgentDraftV1ConvaiAgentsAgentIDDraftsPost](../../models/components/bodycreateagentdraftv1convaiagentsagentiddraftspost.md)          | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |                                                                                                                                                           |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.CreateAgentDraftRouteResponse](../../models/operations/createagentdraftrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAgentDraftRoute

Delete a draft for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_agent_draft_route" method="delete" path="/v1/convai/agents/{agent_id}/drafts" -->
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

    res, err := s.AgentsPlatform.DeleteAgentDraftRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               | Example                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |                                                                                                                                                           |
| `agentID`                                                                                                                                                 | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                        |
| `branchID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | The ID of the agent branch to use                                                                                                                         | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                                                                                                      |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |                                                                                                                                                           |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |                                                                                                                                                           |

### Response

**[*operations.DeleteAgentDraftRouteResponse](../../models/operations/deleteagentdraftrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListEnvironmentVariables

List all environment variables for the workspace with optional filtering

### Example Usage

<!-- UsageSnippet language="go" operationID="list_environment_variables" method="get" path="/v1/convai/environment-variables" -->
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
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.ListEnvironmentVariables(ctx, operations.ListEnvironmentVariablesRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.EnvironmentVariablesListResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                    | :heavy_check_mark:                                                                                       | The context to use for the request.                                                                      |
| `request`                                                                                                | [operations.ListEnvironmentVariablesRequest](../../models/operations/listenvironmentvariablesrequest.md) | :heavy_check_mark:                                                                                       | The request object to use for the request.                                                               |
| `opts`                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                 | :heavy_minus_sign:                                                                                       | The options for this request.                                                                            |

### Response

**[*operations.ListEnvironmentVariablesResponse](../../models/operations/listenvironmentvariablesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateEnvironmentVariable

Create a new environment variable for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="create_environment_variable" method="post" path="/v1/convai/environment-variables" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.CreateEnvironmentVariable(ctx, operations.CreateAgentsPlatformCreateEnvironmentVariableRequestAuthConnection(
        components.CreateAuthConnectionEnvironmentVariableRequest{
            Label: "<value>",
            Values: map[string]components.EnvironmentVariableAuthConnectionValueRequest{

            },
        },
    ), optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.EnvironmentVariableResponse != nil {
        switch res.EnvironmentVariableResponse.Values.Type {
            case components.EnvironmentVariableResponseValuesTypeMapOfStr:
                // res.EnvironmentVariableResponse.Values.MapOfStr is populated
            case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableSecretValue:
                // res.EnvironmentVariableResponse.Values.MapOfEnvironmentVariableSecretValue is populated
            case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableAuthConnectionValue:
                // res.EnvironmentVariableResponse.Values.MapOfEnvironmentVariableAuthConnectionValue is populated
            default:
                // Unknown type - use res.EnvironmentVariableResponse.Values.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `body`                                                                                                                                                    | [operations.AgentsPlatformCreateEnvironmentVariableRequest](../../models/operations/agentsplatformcreateenvironmentvariablerequest.md)                    | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.CreateEnvironmentVariableResponse](../../models/operations/createenvironmentvariableresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetEnvironmentVariable

Get a specific environment variable by ID

### Example Usage

<!-- UsageSnippet language="go" operationID="get_environment_variable" method="get" path="/v1/convai/environment-variables/{env_var_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/components"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        "https://api.example.com",
    )

    res, err := s.AgentsPlatform.GetEnvironmentVariable(ctx, "<id>", optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.EnvironmentVariableResponse != nil {
        switch res.EnvironmentVariableResponse.Values.Type {
            case components.EnvironmentVariableResponseValuesTypeMapOfStr:
                // res.EnvironmentVariableResponse.Values.MapOfStr is populated
            case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableSecretValue:
                // res.EnvironmentVariableResponse.Values.MapOfEnvironmentVariableSecretValue is populated
            case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableAuthConnectionValue:
                // res.EnvironmentVariableResponse.Values.MapOfEnvironmentVariableAuthConnectionValue is populated
            default:
                // Unknown type - use res.EnvironmentVariableResponse.Values.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `envVarID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.GetEnvironmentVariableResponse](../../models/operations/getenvironmentvariableresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateEnvironmentVariable

Replace an environment variable's values. Use null to remove an environment (except production).

### Example Usage

<!-- UsageSnippet language="go" operationID="update_environment_variable" method="patch" path="/v1/convai/environment-variables/{env_var_id}" -->
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

    res, err := s.AgentsPlatform.UpdateEnvironmentVariable(ctx, "<id>", components.UpdateEnvironmentVariableRequest{
        Values: map[string]*components.UpdateEnvironmentVariableRequestValues{

        },
    }, optionalnullable.From[string](nil))
    if err != nil {
        log.Fatal(err)
    }
    if res.EnvironmentVariableResponse != nil {
        switch res.EnvironmentVariableResponse.Values.Type {
            case components.EnvironmentVariableResponseValuesTypeMapOfStr:
                // res.EnvironmentVariableResponse.Values.MapOfStr is populated
            case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableSecretValue:
                // res.EnvironmentVariableResponse.Values.MapOfEnvironmentVariableSecretValue is populated
            case components.EnvironmentVariableResponseValuesTypeMapOfEnvironmentVariableAuthConnectionValue:
                // res.EnvironmentVariableResponse.Values.MapOfEnvironmentVariableAuthConnectionValue is populated
            default:
                // Unknown type - use res.EnvironmentVariableResponse.Values.GetUnknownRaw() for raw JSON
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                 | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                     | :heavy_check_mark:                                                                                                                                        | The context to use for the request.                                                                                                                       |
| `envVarID`                                                                                                                                                | `string`                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `body`                                                                                                                                                    | [components.UpdateEnvironmentVariableRequest](../../models/components/updateenvironmentvariablerequest.md)                                                | :heavy_check_mark:                                                                                                                                        | N/A                                                                                                                                                       |
| `xiAPIKey`                                                                                                                                                | optionalnullable.OptionalNullable[`string`]                                                                                                               | :heavy_minus_sign:                                                                                                                                        | Your API key. This is required by most endpoints to access our API programmatically. You can view your xi-api-key using the 'Profile' tab on the website. |
| `opts`                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                  | :heavy_minus_sign:                                                                                                                                        | The options for this request.                                                                                                                             |

### Response

**[*operations.UpdateEnvironmentVariableResponse](../../models/operations/updateenvironmentvariableresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |