# AgentsPlatform

## Overview

Build, configure and manage Conversational AI agents, knowledge bases, tools, and conversations.

### Available Operations

* [GetConversationSignedLink](#getconversationsignedlink) - Get Signed Url
* [~~GetSignedURLDeprecated~~](#getsignedurldeprecated) - Get Signed Url :warning: **Deprecated**
* [GetLivekitToken](#getlivekittoken) - Get Webrtc Token
* [HandleTwilioOutboundCall](#handletwiliooutboundcall) - Handle An Outbound Call Via Twilio
* [RegisterTwilioCall](#registertwiliocall) - Register A Twilio Call And Return Twiml
* [HandleExotelOutboundCall](#handleexoteloutboundcall) - Handle An Outbound Call Via Exotel
* [WhatsappOutboundCall](#whatsappoutboundcall) - Make An Outbound Call Via Whatsapp
* [WhatsappOutboundMessage](#whatsappoutboundmessage) - Send An Outbound Message Via Whatsapp
* [CreateAgent](#createagent) - Create Agent
* [GetAgentSummaries](#getagentsummaries) - Get Agent Summaries
* [GetAgent](#getagent) - Get Agent
* [PatchAgentSettings](#patchagentsettings) - Patches An Agent Settings
* [DeleteAgent](#deleteagent) - Delete Agent
* [GetAgentWidget](#getagentwidget) - Get Agent Widget Config
* [GetAgentLink](#getagentlink) - Get Shareable Agent Link
* [PostAgentAvatar](#postagentavatar) - Post Agent Avatar
* [GetAgents](#getagents) - List Agents
* [GetAgentKnowledgeBaseSize](#getagentknowledgebasesize) - Returns The Size Of The Agent'S Knowledge Base
* [GetAgentLlmExpectedCostCalculation](#getagentllmexpectedcostcalculation) - Calculate Expected Llm Usage For An Agent
* [DuplicateAgent](#duplicateagent) - Duplicate Agent
* [~~RunConversationSimulation~~](#runconversationsimulation) - Simulates A Conversation :warning: **Deprecated**
* [~~RunConversationSimulationRouteStream~~](#runconversationsimulationroutestream) - Simulates A Conversation (Stream) :warning: **Deprecated**
* [CreateAgentTestFolder](#createagenttestfolder) - Create Agent Test Folder
* [GetAgentTestFolder](#getagenttestfolder) - Get Agent Test Folder By Id
* [UpdateAgentTestFolder](#updateagenttestfolder) - Update Agent Test Folder
* [DeleteAgentTestFolder](#deleteagenttestfolder) - Delete Agent Test Folder
* [AgentTestingBulkMove](#agenttestingbulkmove) - Bulk Move Tests To Folder
* [GetConversationHistories](#getconversationhistories) - Get Conversations
* [GetConversationUsers](#getconversationusers) - Get Conversation Users
* [GetConversationHistory](#getconversationhistory) - Get Conversation Details
* [DeleteConversation](#deleteconversation) - Delete Conversation
* [GetConversationSipMessages](#getconversationsipmessages) - Get Sip Messages For A Conversation
* [GetConversationAudio](#getconversationaudio) - Get Conversation Audio
* [PostConversationFeedback](#postconversationfeedback) - Send Conversation Feedback
* [TextSearchConversationMessages](#textsearchconversationmessages) - Text Search Conversation Messages
* [SmartSearchConversationMessages](#smartsearchconversationmessages) - Smart Search Conversation Messages
* [AssignConversationTagsRoute](#assignconversationtagsroute) - Assign Conversation Tags
* [UnassignConversationTagRoute](#unassignconversationtagroute) - Unassign Conversation Tag
* [ListConversationTagsRoute](#listconversationtagsroute) - List Conversation Tags
* [CreateConversationTagRoute](#createconversationtagroute) - Create Conversation Tag
* [GetConversationTagRoute](#getconversationtagroute) - Get Conversation Tag
* [DeleteConversationTagRoute](#deleteconversationtagroute) - Delete Conversation Tag
* [UpdateConversationTagRoute](#updateconversationtagroute) - Update Conversation Tag
* [CreatePhoneNumber](#createphonenumber) - Import Phone Number
* [ListPhoneNumbers](#listphonenumbers) - List Phone Numbers
* [GetPhoneNumber](#getphonenumber) - Get Phone Number
* [DeletePhoneNumber](#deletephonenumber) - Delete Phone Number
* [UpdatePhoneNumber](#updatephonenumber) - Update Phone Number
* [ListSipMessages](#listsipmessages) - Get Sip Messages For A Phone Number
* [GetPublicLlmExpectedCostCalculation](#getpublicllmexpectedcostcalculation) - Calculate Expected Llm Usage
* [ListAvailableLlms](#listavailablellms) - List Available Llms
* [UploadFile](#uploadfile) - Upload File
* [CancelFileUpload](#cancelfileupload) - Delete File Upload
* [GetLiveCount](#getlivecount) - Get Live Count
* [GetAgentKnowledgeBaseSummaries](#getagentknowledgebasesummaries) - Get Knowledge Base Summaries By Ids
* [GetKnowledgeBaseList](#getknowledgebaselist) - Get Knowledge Base List
* [~~AddDocumentationToKnowledgeBase~~](#adddocumentationtoknowledgebase) - Add To Knowledge Base :warning: **Deprecated**
* [CreateURLDocument](#createurldocument) - Create Url Document
* [CreateFileDocument](#createfiledocument) - Create File Document
* [CreateTextDocument](#createtextdocument) - Create Text Document
* [UpdateDocument](#updatedocument) - Update Document
* [GetDocumentationFromKnowledgeBase](#getdocumentationfromknowledgebase) - Get Documentation From Knowledge Base
* [DeleteKnowledgeBaseDocument](#deleteknowledgebasedocument) - Delete Knowledge Base Document Or Folder
* [UpdateFileDocumentRoute](#updatefiledocumentroute) - Update File Document
* [GetRagIndexOverview](#getragindexoverview) - Get Rag Index Overview.
* [GetOrCreateRagIndexes](#getorcreateragindexes) - Compute Rag Indexes In Batch
* [RefreshURLDocument](#refreshurldocument) - Refresh Url Document Content
* [GetRagIndexes](#getragindexes) - Get Rag Indexes Of The Specified Knowledgebase Document.
* [RagIndexStatus](#ragindexstatus) - Compute Rag Index.
* [DeleteRagIndex](#deleteragindex) - Delete Rag Index.
* [SearchKnowledgeBaseContent](#searchknowledgebasecontent) - Search Knowledge Base Content
* [GetKnowledgeBaseDependentAgents](#getknowledgebasedependentagents) - Get Dependent Agents List
* [GetKnowledgeBaseContent](#getknowledgebasecontent) - Get Document Content
* [GetKnowledgeBaseSourceFileURL](#getknowledgebasesourcefileurl) - Get Document Source File Url
* [GetDocumentationChunkFromKnowledgeBase](#getdocumentationchunkfromknowledgebase) - Get Documentation Chunk From Knowledge Base
* [GetDocumentationChunksFromKnowledgeBase](#getdocumentationchunksfromknowledgebase) - Get All Rag Chunks For A Document
* [GetAgentTopicsRoute](#getagenttopicsroute) - Get Agent Conversation Topics
* [AddTool](#addtool) - Add Tool
* [GetTools](#gettools) - Get Tools
* [GetTool](#gettool) - Get Tool
* [UpdateTool](#updatetool) - Update Tool
* [DeleteTool](#deletetool) - Delete Tool
* [GetToolDependentAgents](#gettooldependentagents) - Get Dependent Agents List
* [GetToolExecutionsRoute](#gettoolexecutionsroute) - Get Tool Executions
* [GetSettings](#getsettings) - Get Convai Settings
* [UpdateSettings](#updatesettings) - Update Convai Settings
* [GetDashboardSettings](#getdashboardsettings) - Get Convai Dashboard Settings
* [UpdateDashboardSettings](#updatedashboardsettings) - Update Convai Dashboard Settings
* [CreateSecret](#createsecret) - Create Convai Workspace Secret
* [GetSecrets](#getsecrets) - Get Convai Workspace Secrets
* [GetSecretRoute](#getsecretroute) - Get Convai Workspace Secret
* [DeleteSecret](#deletesecret) - Delete Convai Workspace Secret
* [UpdateSecret](#updatesecret) - Update Convai Workspace Secret
* [GetSecretDependencies](#getsecretdependencies) - Get Secret Dependencies By Type
* [CreateBatchCall](#createbatchcall) - Submit A Batch Call Request.
* [GetWorkspaceBatchCalls](#getworkspacebatchcalls) - Get All Batch Calls For A Workspace.
* [GetBatchCall](#getbatchcall) - Get A Batch Call By Id.
* [DeleteBatchCall](#deletebatchcall) - Delete A Batch Call.
* [CancelBatchCall](#cancelbatchcall) - Cancel A Batch Call.
* [RetryBatchCall](#retrybatchcall) - Retry A Batch Call.
* [HandleSipTrunkOutboundCall](#handlesiptrunkoutboundcall) - Handle An Outbound Call Via Sip Trunk
* [CreateMcpServer](#createmcpserver) - Create Mcp Server
* [ListMcpServers](#listmcpservers) - List Mcp Servers
* [GetMcp](#getmcp) - Get Mcp Server
* [DeleteMcpServer](#deletemcpserver) - Delete Mcp Server
* [UpdateMcpServerConfig](#updatemcpserverconfig) - Update Mcp Server Configuration
* [ListMcpServerTools](#listmcpservertools) - List Mcp Server Tools
* [~~UpdateMcpServerApprovalPolicy~~](#updatemcpserverapprovalpolicy) - Update Mcp Server Approval Policy :warning: **Deprecated**
* [AddMcpServerToolApproval](#addmcpservertoolapproval) - Create Mcp Server Tool Approval
* [RemoveMcpServerToolApproval](#removemcpservertoolapproval) - Delete Mcp Server Tool Approval
* [AddMcpToolConfigOverride](#addmcptoolconfigoverride) - Create Mcp Tool Configuration Override
* [GetMcpToolConfigOverride](#getmcptoolconfigoverride) - Get Mcp Tool Configuration Override
* [UpdateMcpToolConfigOverride](#updatemcptoolconfigoverride) - Update Mcp Tool Configuration Override
* [RemoveMcpToolConfigOverride](#removemcptoolconfigoverride) - Delete Mcp Tool Configuration Override
* [GetWhatsappAccount](#getwhatsappaccount) - Get Whatsapp Account
* [DeleteWhatsappAccount](#deletewhatsappaccount) - Delete Whatsapp Account
* [UpdateWhatsappAccount](#updatewhatsappaccount) - Update Whatsapp Account
* [ListWhatsappAccounts](#listwhatsappaccounts) - List Whatsapp Accounts
* [CreateBranch](#createbranch) - Create A New Branch
* [GetBranches](#getbranches) - List Agent Branches
* [GetBranch](#getbranch) - Get Agent Branch
* [UpdateBranch](#updatebranch) - Update Agent Branch
* [GetVersionMetadataRoute](#getversionmetadataroute) - Get Agent Version Metadata
* [MergePreviewRoute](#mergepreviewroute) - Preview Merged Configuration
* [MergeBranchIntoTarget](#mergebranchintotarget) - Merge A Branch Into A Target Branch
* [RebasePreviewRoute](#rebasepreviewroute) - Preview Rebased Configuration
* [RebaseBranchOntoMain](#rebasebranchontomain) - Rebase A Branch Onto Main
* [CreateAgentDeployment](#createagentdeployment) - Create Or Update Deployments
* [CreateAgentDraft](#createagentdraft) - Create Agent Draft
* [DeleteAgentDraft](#deleteagentdraft) - Delete Agent Draft
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetConversationSignedLink(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(false), nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationSignedURLResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                             | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           | Example                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                 | :heavy_check_mark:                                                                                                    | The context to use for the request.                                                                                   |                                                                                                                       |
| `agentID`                                                                                                             | `string`                                                                                                              | :heavy_check_mark:                                                                                                    | Agent id (agent_…) or speech engine external id (seng_), resolved to the same underlying resource.                    | **Example 1:** agent_3701k3ttaq12ewp8b7qv5rfyszkz<br/>**Example 2:** seng_3701k3ttaq12ewp8b7qv5rfyszkz                |
| `includeConversationID`                                                                                               | `*bool`                                                                                                               | :heavy_minus_sign:                                                                                                    | Whether to include a conversation_id with the response. If included, the conversation_signature cannot be used again. |                                                                                                                       |
| `branchID`                                                                                                            | `*string`                                                                                                             | :heavy_minus_sign:                                                                                                    | The ID of the branch to use                                                                                           |                                                                                                                       |
| `environment`                                                                                                         | `*string`                                                                                                             | :heavy_minus_sign:                                                                                                    | The environment to use for resolving environment variables (e.g. 'production', 'staging'). Defaults to 'production'.  |                                                                                                                       |
| `opts`                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                              | :heavy_minus_sign:                                                                                                    | The options for this request.                                                                                         |                                                                                                                       |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetSignedURLDeprecated(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(false), nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationSignedURLResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                             | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           | Example                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                 | :heavy_check_mark:                                                                                                    | The context to use for the request.                                                                                   |                                                                                                                       |
| `agentID`                                                                                                             | `string`                                                                                                              | :heavy_check_mark:                                                                                                    | Agent id (agent_…) or speech engine external id (seng_), resolved to the same underlying resource.                    | **Example 1:** agent_3701k3ttaq12ewp8b7qv5rfyszkz<br/>**Example 2:** seng_3701k3ttaq12ewp8b7qv5rfyszkz                |
| `includeConversationID`                                                                                               | `*bool`                                                                                                               | :heavy_minus_sign:                                                                                                    | Whether to include a conversation_id with the response. If included, the conversation_signature cannot be used again. |                                                                                                                       |
| `branchID`                                                                                                            | `*string`                                                                                                             | :heavy_minus_sign:                                                                                                    | The ID of the branch to use                                                                                           |                                                                                                                       |
| `environment`                                                                                                         | `*string`                                                                                                             | :heavy_minus_sign:                                                                                                    | The environment to use for resolving environment variables (e.g. 'production', 'staging'). Defaults to 'production'.  |                                                                                                                       |
| `opts`                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                              | :heavy_minus_sign:                                                                                                    | The options for this request.                                                                                         |                                                                                                                       |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetLivekitToken(ctx, "21m00Tcm4TlvDq8ikWAM", nil, nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.TokenResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                            | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          | Example                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                | :heavy_check_mark:                                                                                                   | The context to use for the request.                                                                                  |                                                                                                                      |
| `agentID`                                                                                                            | `string`                                                                                                             | :heavy_check_mark:                                                                                                   | Agent id (agent_…) or speech engine external id (seng_), resolved to the same underlying resource.                   | **Example 1:** agent_3701k3ttaq12ewp8b7qv5rfyszkz<br/>**Example 2:** seng_3701k3ttaq12ewp8b7qv5rfyszkz               |
| `participantName`                                                                                                    | `*string`                                                                                                            | :heavy_minus_sign:                                                                                                   | Optional custom participant name. If not provided, user ID will be used                                              |                                                                                                                      |
| `branchID`                                                                                                           | `*string`                                                                                                            | :heavy_minus_sign:                                                                                                   | The ID of the branch to use                                                                                          |                                                                                                                      |
| `environment`                                                                                                        | `*string`                                                                                                            | :heavy_minus_sign:                                                                                                   | The environment to use for resolving environment variables (e.g. 'production', 'staging'). Defaults to 'production'. |                                                                                                                      |
| `opts`                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                             | :heavy_minus_sign:                                                                                                   | The options for this request.                                                                                        |                                                                                                                      |

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
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.HandleTwilioOutboundCall(ctx, components.BodyHandleAnOutboundCallViaTwilioV1ConvaiTwilioOutboundCallPost{
        AgentID: "<id>",
        AgentPhoneNumberID: "<id>",
        ToNumber: "<value>",
        ConversationInitiationClientData: &components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Asr: &components.ASRConversationalConfigOverride{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfigOverride{
                    SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                        Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                    },
                },
                Tts: &components.TTSConversationalConfigOverride{
                    VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                    Stability: elevenlabsgo.Pointer[float64](0.5),
                    Speed: elevenlabsgo.Pointer[float64](1.0),
                    SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                },
                Agent: &components.AgentConfigOverrideInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                    Language: elevenlabsgo.Pointer("en"),
                    Prompt: &components.PromptAgentAPIModelOverrideInput{
                        Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                        Llm: components.LlmGemini20Flash001.ToPointer(),
                        ToolIds: []string{},
                        KnowledgeBase: []components.KnowledgeBaseLocator{},
                    },
                },
            },
        },
    })
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
| `request`                                                                                                                                                                | [components.BodyHandleAnOutboundCallViaTwilioV1ConvaiTwilioOutboundCallPost](../../models/components/bodyhandleanoutboundcallviatwiliov1convaitwiliooutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                       | The request object to use for the request.                                                                                                                               |
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
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.RegisterTwilioCall(ctx, components.BodyRegisterATwilioCallAndReturnTwiMLV1ConvaiTwilioRegisterCallPost{
        AgentID: "<id>",
        FromNumber: "<value>",
        ToNumber: "<value>",
        ConversationInitiationClientData: &components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Asr: &components.ASRConversationalConfigOverride{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfigOverride{
                    SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                        Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                    },
                },
                Tts: &components.TTSConversationalConfigOverride{
                    VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                    Stability: elevenlabsgo.Pointer[float64](0.5),
                    Speed: elevenlabsgo.Pointer[float64](1.0),
                    SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                },
                Agent: &components.AgentConfigOverrideInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                    Language: elevenlabsgo.Pointer("en"),
                    Prompt: &components.PromptAgentAPIModelOverrideInput{
                        Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                        Llm: components.LlmGemini20Flash001.ToPointer(),
                        ToolIds: []string{},
                        KnowledgeBase: []components.KnowledgeBaseLocator{},
                    },
                },
            },
        },
    })
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
| `request`                                                                                                                                                                        | [components.BodyRegisterATwilioCallAndReturnTwiMLV1ConvaiTwilioRegisterCallPost](../../models/components/bodyregisteratwiliocallandreturntwimlv1convaitwilioregistercallpost.md) | :heavy_check_mark:                                                                                                                                                               | The request object to use for the request.                                                                                                                                       |
| `opts`                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                         | :heavy_minus_sign:                                                                                                                                                               | The options for this request.                                                                                                                                                    |

### Response

**[*operations.RegisterTwilioCallResponse](../../models/operations/registertwiliocallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## HandleExotelOutboundCall

Handle an outbound call via Exotel Connect API

### Example Usage

<!-- UsageSnippet language="go" operationID="handle_exotel_outbound_call" method="post" path="/v1/convai/exotel/outbound-call" -->
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

    res, err := s.AgentsPlatform.HandleExotelOutboundCall(ctx, components.BodyHandleAnOutboundCallViaExotelV1ConvaiExotelOutboundCallPost{
        AgentID: "<id>",
        AgentPhoneNumberID: "<id>",
        ToNumber: "<value>",
        ConversationInitiationClientData: &components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Asr: &components.ASRConversationalConfigOverride{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfigOverride{
                    SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                        Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                    },
                },
                Tts: &components.TTSConversationalConfigOverride{
                    VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                    Stability: elevenlabsgo.Pointer[float64](0.5),
                    Speed: elevenlabsgo.Pointer[float64](1.0),
                    SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                },
                Agent: &components.AgentConfigOverrideInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                    Language: elevenlabsgo.Pointer("en"),
                    Prompt: &components.PromptAgentAPIModelOverrideInput{
                        Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                        Llm: components.LlmGemini20Flash001.ToPointer(),
                        ToolIds: []string{},
                        KnowledgeBase: []components.KnowledgeBaseLocator{},
                    },
                },
            },
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ExotelOutboundCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                | Type                                                                                                                                                                     | Required                                                                                                                                                                 | Description                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                    | :heavy_check_mark:                                                                                                                                                       | The context to use for the request.                                                                                                                                      |
| `request`                                                                                                                                                                | [components.BodyHandleAnOutboundCallViaExotelV1ConvaiExotelOutboundCallPost](../../models/components/bodyhandleanoutboundcallviaexotelv1convaiexoteloutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                       | The request object to use for the request.                                                                                                                               |
| `opts`                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                 | :heavy_minus_sign:                                                                                                                                                       | The options for this request.                                                                                                                                            |

### Response

**[*operations.HandleExotelOutboundCallResponse](../../models/operations/handleexoteloutboundcallresponse.md), error**

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
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.WhatsappOutboundCall(ctx, components.BodyMakeAnOutboundCallViaWhatsAppV1ConvaiWhatsappOutboundCallPost{
        WhatsappPhoneNumberID: "<id>",
        WhatsappUserID: "<id>",
        WhatsappCallPermissionRequestTemplateName: "<value>",
        WhatsappCallPermissionRequestTemplateLanguageCode: "<value>",
        AgentID: "<id>",
        ConversationInitiationClientData: &components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Asr: &components.ASRConversationalConfigOverride{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfigOverride{
                    SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                        Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                    },
                },
                Tts: &components.TTSConversationalConfigOverride{
                    VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                    Stability: elevenlabsgo.Pointer[float64](0.5),
                    Speed: elevenlabsgo.Pointer[float64](1.0),
                    SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                },
                Agent: &components.AgentConfigOverrideInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                    Language: elevenlabsgo.Pointer("en"),
                    Prompt: &components.PromptAgentAPIModelOverrideInput{
                        Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                        Llm: components.LlmGemini20Flash001.ToPointer(),
                        ToolIds: []string{},
                        KnowledgeBase: []components.KnowledgeBaseLocator{},
                    },
                },
            },
        },
    })
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
| `request`                                                                                                                                                                    | [components.BodyMakeAnOutboundCallViaWhatsAppV1ConvaiWhatsappOutboundCallPost](../../models/components/bodymakeanoutboundcallviawhatsappv1convaiwhatsappoutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                           | The request object to use for the request.                                                                                                                                   |
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.WhatsappOutboundMessage(ctx, components.BodySendAnOutboundMessageViaWhatsAppV1ConvaiWhatsappOutboundMessagePost{
        WhatsappPhoneNumberID: "<id>",
        WhatsappUserID: "<id>",
        TemplateName: "<value>",
        TemplateLanguageCode: "<value>",
        TemplateParams: []components.TemplateParam{},
        AgentID: "<id>",
        ConversationInitiationClientData: &components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Asr: &components.ASRConversationalConfigOverride{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfigOverride{
                    SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                        Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                    },
                },
                Tts: &components.TTSConversationalConfigOverride{
                    VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                    Stability: elevenlabsgo.Pointer[float64](0.5),
                    Speed: elevenlabsgo.Pointer[float64](1.0),
                    SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                },
                Agent: &components.AgentConfigOverrideInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                    Language: elevenlabsgo.Pointer("en"),
                    Prompt: &components.PromptAgentAPIModelOverrideInput{
                        Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                        Llm: components.LlmGemini20Flash001.ToPointer(),
                        ToolIds: []string{},
                        KnowledgeBase: []components.KnowledgeBaseLocator{},
                    },
                },
            },
        },
    })
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
| `request`                                                                                                                                                                                | [components.BodySendAnOutboundMessageViaWhatsAppV1ConvaiWhatsappOutboundMessagePost](../../models/components/bodysendanoutboundmessageviawhatsappv1convaiwhatsappoutboundmessagepost.md) | :heavy_check_mark:                                                                                                                                                                       | The request object to use for the request.                                                                                                                                               |
| `opts`                                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                       | The options for this request.                                                                                                                                                            |

### Response

**[*operations.WhatsappOutboundMessageResponse](../../models/operations/whatsappoutboundmessageresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgent

Create an agent from a config object

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_route" method="post" path="/v1/convai/agents/create" -->
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

    res, err := s.AgentsPlatform.CreateAgent(ctx, components.BodyCreateAgentV1ConvaiAgentsCreatePost{
        ConversationConfig: components.ConversationalConfigAPIModelInput{
            Asr: &components.ASRConversationalConfig{
                Keywords: []string{
                    "hello",
                    "world",
                },
            },
            Turn: &components.TurnConfig{
                InterruptionIgnoreTerms: []string{},
                SoftTimeoutConfig: &components.SoftTimeoutConfig{},
            },
            Tts: &components.TTSConversationalConfigInput{
                ModelID: components.TTSConversationalModelElevenTurboV2.ToPointer(),
                OptimizeStreamingLatency: components.TTSOptimizeStreamingLatencyThree.ToPointer(),
                PronunciationDictionaryLocators: []components.PydanticPronunciationDictionaryVersionLocator{},
            },
            Conversation: &components.ConversationConfigInput{
                ClientEvents: []components.ClientEvent{
                    components.ClientEventAudio,
                    components.ClientEventInterruption,
                },
            },
            LanguagePresets: map[string]components.LanguagePresetInput{
                "key": components.LanguagePresetInput{
                    Overrides: components.ConversationConfigClientOverrideInput{
                        Turn: &components.TurnConfigOverride{
                            SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                                Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                            },
                        },
                        Tts: &components.TTSConversationalConfigOverride{
                            VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                            Stability: elevenlabsgo.Pointer[float64](0.5),
                            Speed: elevenlabsgo.Pointer[float64](1.0),
                            SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                        },
                        Agent: &components.AgentConfigOverrideInput{
                            FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                            Language: elevenlabsgo.Pointer("en"),
                            Prompt: &components.PromptAgentAPIModelOverrideInput{
                                Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                                Llm: components.LlmGemini20Flash001.ToPointer(),
                                ToolIds: []string{},
                                KnowledgeBase: []components.KnowledgeBaseLocator{},
                            },
                        },
                    },
                },
            },
            Vad: &components.VADConfig{},
            Agent: &components.AgentConfigAPIModelInput{
                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
            },
        },
        PlatformSettings: &components.AgentPlatformSettingsRequestModel{
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
                CustomAvatarPath: elevenlabsgo.Pointer("https://example.com/avatar.png"),
            },
            DataCollection: map[string]components.AnalysisProperty{
                "key": components.AnalysisProperty{
                    Type: components.AnalysisPropertyTypeString,
                    Description: elevenlabsgo.Pointer("A user-provided message"),
                },
            },
            Overrides: &components.ConversationInitiationClientDataConfigInput{
                CustomLlmExtraBody: elevenlabsgo.Pointer(true),
                EnableConversationInitiationClientDataFromWebhook: elevenlabsgo.Pointer(true),
                EnableStartingWorkflowNodeIDFromClient: elevenlabsgo.Pointer(true),
            },
            WorkspaceOverrides: &components.AgentWorkspaceOverridesInput{
                ConversationInitiationClientDataWebhook: &components.ConversationInitiationClientDataWebhook{
                    URL: "https://example.com/webhook",
                    RequestHeaders: map[string]components.ConversationInitiationClientDataWebhookRequestHeaders{
                        "Content-Type": components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(
                            "application/json",
                        ),
                    },
                },
            },
            Testing: &components.AgentTestingSettings{
                AttachedTests: []components.AttachedTestModel{
                    components.AttachedTestModel{
                        TestID: "test_123",
                        WorkflowNodeID: elevenlabsgo.Pointer("node_abc"),
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
                ShareableToken: elevenlabsgo.Pointer("1234567890"),
            },
            CallLimits: &components.AgentCallLimits{},
            Privacy: &components.PrivacyConfigInput{},
        },
        Workflow: &components.AgentWorkflowRequestModel{
            Edges: map[string]components.WorkflowEdgeModelInput{
                "entry_to_tool_a": components.WorkflowEdgeModelInput{
                    Source: "entry_node",
                    Target: "tool_node_a",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: true,
                        },
                    )),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputStringLiteral(
                                components.ASTStringNodeInput{
                                    Value: "<value>",
                                },
                            ),
                        },
                    )),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
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
                        AgentID: elevenlabsgo.Pointer("<id>"),
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
        Name: elevenlabsgo.Pointer("My agent"),
        Tags: []string{
            "Customer Support",
            "Technical Help",
            "Eleven",
        },
    }, elevenlabsgo.Pointer(true))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                 | Type                                                                                                                                                                                      | Required                                                                                                                                                                                  | Description                                                                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                        | The context to use for the request.                                                                                                                                                       |
| `body`                                                                                                                                                                                    | [components.BodyCreateAgentV1ConvaiAgentsCreatePost](../../models/components/bodycreateagentv1convaiagentscreatepost.md)                                                                  | :heavy_check_mark:                                                                                                                                                                        | N/A                                                                                                                                                                                       |
| `enableVersioning`                                                                                                                                                                        | `*bool`                                                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                                        | : warning: ** DEPRECATED **: This will be removed in a future release, please migrate away from it as soon as possible.<br/><br/>Deprecated: all agents are versioned. This parameter is ignored. |
| `opts`                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                        | The options for this request.                                                                                                                                                             |

### Response

**[*operations.CreateAgentRouteResponse](../../models/operations/createagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentSummaries

Returns summaries for the specified agents.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_summaries_route" method="get" path="/v1/convai/agents/summaries" -->
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

    res, err := s.AgentsPlatform.GetAgentSummaries(ctx, []string{
        "J3Pbu5gP6NNKBscdCdwB",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetAgentSummariesV1ConvaiAgentsSummariesGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 | Example                                                                     |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `ctx`                                                                       | [context.Context](https://pkg.go.dev/context#Context)                       | :heavy_check_mark:                                                          | The context to use for the request.                                         |                                                                             |
| `agentIds`                                                                  | []`string`                                                                  | :heavy_check_mark:                                                          | List of agent IDs to fetch summaries for                                    | **Example 1:** J3Pbu5gP6NNKBscdCdwB<br/>**Example 2:** K4Qcu6hQ7OOLCtdeDeXC |
| `opts`                                                                      | [][operations.Option](../../models/operations/option.md)                    | :heavy_minus_sign:                                                          | The options for this request.                                               |                                                                             |

### Response

**[*operations.GetAgentSummariesRouteResponse](../../models/operations/getagentsummariesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgent

Retrieve config for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_route" method="get" path="/v1/convai/agents/{agent_id}" -->
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

    res, err := s.AgentsPlatform.GetAgent(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", elevenlabsgo.Pointer("agtvrsn_8901k4t9z5defmb8vh3e9361y7nj"), elevenlabsgo.Pointer("agtbranch_0901k4aafjxxfxt93gd841r7tv5t"))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `versionID`                                              | `*string`                                                | :heavy_minus_sign:                                       | The ID of the agent version to use                       | agtvrsn_8901k4t9z5defmb8vh3e9361y7nj                     |
| `branchID`                                               | `*string`                                                | :heavy_minus_sign:                                       | The ID of the branch to use                              | agtbranch_0901k4aafjxxfxt93gd841r7tv5t                   |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetAgentRouteResponse](../../models/operations/getagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PatchAgentSettings

Patches an Agent settings

### Example Usage

<!-- UsageSnippet language="go" operationID="patch_agent_settings_route" method="patch" path="/v1/convai/agents/{agent_id}" -->
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

    res, err := s.AgentsPlatform.PatchAgentSettings(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", elevenlabsgo.Pointer(true), elevenlabsgo.Pointer("agtbranch_0901k4aafjxxfxt93gd841r7tv5t"), &components.BodyPatchesAnAgentSettingsV1ConvaiAgentsAgentIDPatch{
        Workflow: &components.AgentWorkflowRequestModel{
            Edges: map[string]components.WorkflowEdgeModelInput{
                "entry_to_tool_a": components.WorkflowEdgeModelInput{
                    Source: "entry_node",
                    Target: "tool_node_a",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: false,
                        },
                    )),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: false,
                        },
                    )),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: true,
                        },
                    )),
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
                        AgentID: elevenlabsgo.Pointer("<id>"),
                    },
                ),
                "success_phone": components.CreateAgentWorkflowRequestModelNodesTool(
                    components.WorkflowToolNodeModelInput{},
                ),
                "success_transfer": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: elevenlabsgo.Pointer("<id>"),
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
        Name: elevenlabsgo.Pointer("My agent"),
        Tags: []string{
            "Customer Support",
            "Technical Help",
            "Eleven",
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

| Parameter                                                                                                                                                                                 | Type                                                                                                                                                                                      | Required                                                                                                                                                                                  | Description                                                                                                                                                                               | Example                                                                                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                        | The context to use for the request.                                                                                                                                                       |                                                                                                                                                                                           |
| `agentID`                                                                                                                                                                                 | `string`                                                                                                                                                                                  | :heavy_check_mark:                                                                                                                                                                        | The id of an agent. This is returned on agent creation.                                                                                                                                   | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                                                        |
| `enableVersioningIfNotEnabled`                                                                                                                                                            | `*bool`                                                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                                                        | : warning: ** DEPRECATED **: This will be removed in a future release, please migrate away from it as soon as possible.<br/><br/>Deprecated: all agents are versioned. This parameter is ignored. |                                                                                                                                                                                           |
| `branchID`                                                                                                                                                                                | `*string`                                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                        | The ID of the branch to use                                                                                                                                                               | agtbranch_0901k4aafjxxfxt93gd841r7tv5t                                                                                                                                                    |
| `body`                                                                                                                                                                                    | [*components.BodyPatchesAnAgentSettingsV1ConvaiAgentsAgentIDPatch](../../models/components/bodypatchesanagentsettingsv1convaiagentsagentidpatch.md)                                       | :heavy_minus_sign:                                                                                                                                                                        | N/A                                                                                                                                                                                       |                                                                                                                                                                                           |
| `opts`                                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                                        | The options for this request.                                                                                                                                                             |                                                                                                                                                                                           |

### Response

**[*operations.PatchAgentSettingsRouteResponse](../../models/operations/patchagentsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAgent

Delete an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_agent_route" method="delete" path="/v1/convai/agents/{agent_id}" -->
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

    res, err := s.AgentsPlatform.DeleteAgent(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteAgentRouteResponse](../../models/operations/deleteagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentWidget

Retrieve the widget configuration for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_widget_route" method="get" path="/v1/convai/agents/{agent_id}/widget" -->
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

    res, err := s.AgentsPlatform.GetAgentWidget(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", nil)
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
| `conversationSignature`                                                                                                                                         | `*string`                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                              | An expiring token that enables a websocket conversation to start. These can be generated for an agent using the /v1/convai/conversation/get_signed_url endpoint |                                                                                                                                                                 |
| `opts`                                                                                                                                                          | [][operations.Option](../../models/operations/option.md)                                                                                                        | :heavy_minus_sign:                                                                                                                                              | The options for this request.                                                                                                                                   |                                                                                                                                                                 |

### Response

**[*operations.GetAgentWidgetRouteResponse](../../models/operations/getagentwidgetrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentLink

Get the current link used to share the agent with others

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_link_route" method="get" path="/v1/convai/agents/{agent_id}/link" -->
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

    res, err := s.AgentsPlatform.GetAgentLink(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentLinkResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetAgentLinkRouteResponse](../../models/operations/getagentlinkrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PostAgentAvatar

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.PostAgentAvatar(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodyPostAgentAvatarV1ConvaiAgentsAgentIDAvatarPost{
        AvatarFile: components.AvatarFile{
            FileName: "example.file",
            Content: example,
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.PostAgentAvatarResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                      | Type                                                                                                                                           | Required                                                                                                                                       | Description                                                                                                                                    | Example                                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                                                          | :heavy_check_mark:                                                                                                                             | The context to use for the request.                                                                                                            |                                                                                                                                                |
| `agentID`                                                                                                                                      | `string`                                                                                                                                       | :heavy_check_mark:                                                                                                                             | The id of an agent. This is returned on agent creation.                                                                                        | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                             |
| `body`                                                                                                                                         | [components.BodyPostAgentAvatarV1ConvaiAgentsAgentIDAvatarPost](../../models/components/bodypostagentavatarv1convaiagentsagentidavatarpost.md) | :heavy_check_mark:                                                                                                                             | N/A                                                                                                                                            |                                                                                                                                                |
| `opts`                                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                                       | :heavy_minus_sign:                                                                                                                             | The options for this request.                                                                                                                  |                                                                                                                                                |

### Response

**[*operations.PostAgentAvatarRouteResponse](../../models/operations/postagentavatarrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgents

Returns a list of your agents and their metadata.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agents_route" method="get" path="/v1/convai/agents" -->
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

    res, err := s.AgentsPlatform.GetAgents(ctx, operations.GetAgentsRouteRequest{
        Archived: elevenlabsgo.Pointer(false),
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetAgentKnowledgeBaseSize(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentKnowledgebaseSizeResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetAgentLlmExpectedCostCalculation(ctx, "<id>", components.LLMUsageCalculatorRequestModel{})
    if err != nil {
        log.Fatal(err)
    }
    if res.LLMUsageCalculatorResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |
| `agentID`                                                                                              | `string`                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `body`                                                                                                 | [components.LLMUsageCalculatorRequestModel](../../models/components/llmusagecalculatorrequestmodel.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |

### Response

**[*operations.GetAgentLlmExpectedCostCalculationResponse](../../models/operations/getagentllmexpectedcostcalculationresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DuplicateAgent

Create a new agent by duplicating an existing one

### Example Usage

<!-- UsageSnippet language="go" operationID="duplicate_agent_route" method="post" path="/v1/convai/agents/{agent_id}/duplicate" -->
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

    res, err := s.AgentsPlatform.DuplicateAgent(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", &components.BodyDuplicateAgentV1ConvaiAgentsAgentIDDuplicatePost{
        Name: elevenlabsgo.Pointer("My agent"),
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

| Parameter                                                                                                                                           | Type                                                                                                                                                | Required                                                                                                                                            | Description                                                                                                                                         | Example                                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                               | :heavy_check_mark:                                                                                                                                  | The context to use for the request.                                                                                                                 |                                                                                                                                                     |
| `agentID`                                                                                                                                           | `string`                                                                                                                                            | :heavy_check_mark:                                                                                                                                  | The id of an agent. This is returned on agent creation.                                                                                             | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                  |
| `body`                                                                                                                                              | [*components.BodyDuplicateAgentV1ConvaiAgentsAgentIDDuplicatePost](../../models/components/bodyduplicateagentv1convaiagentsagentidduplicatepost.md) | :heavy_minus_sign:                                                                                                                                  | N/A                                                                                                                                                 |                                                                                                                                                     |
| `opts`                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                            | :heavy_minus_sign:                                                                                                                                  | The options for this request.                                                                                                                       |                                                                                                                                                     |

### Response

**[*operations.DuplicateAgentRouteResponse](../../models/operations/duplicateagentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ~~RunConversationSimulation~~

Deprecated. Use the `/v1/convai/agent-testing/create` and `/v1/convai/agents/:agent_id/run-tests` endpoints to create and run simulations. Run a conversation between the agent and a simulated user.

> :warning: **DEPRECATED**: This will be removed in a future release, please migrate away from it as soon as possible.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_simulation_route" method="post" path="/v1/convai/agents/{agent_id}/simulate-conversation" -->
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

    res, err := s.AgentsPlatform.RunConversationSimulation(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodySimulatesAConversationV1ConvaiAgentsAgentIDSimulateConversationPost{
        SimulationSpecification: components.ConversationSimulationSpecification{
            SimulatedUserConfig: components.AgentConfigAPIModelInput{
                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
            },
        },
        ExtraEvaluationCriteria: []components.PromptEvaluationCriteria{
            components.PromptEvaluationCriteria{
                ID: "1234567890",
                Name: "Customer satisfaction check",
                ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
            },
        },
    })
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
| `opts`                                                                                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                                       | The options for this request.                                                                                                                                                            |                                                                                                                                                                                          |

### Response

**[*operations.RunConversationSimulationRouteResponse](../../models/operations/runconversationsimulationrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ~~RunConversationSimulationRouteStream~~

Deprecated. Use the `/v1/convai/agent-testing/create` and `/v1/convai/agents/:agent_id/run-tests` endpoints to create and run simulations. Run a conversation between the agent and a simulated user and stream back the response. Response is streamed back as partial lists of messages that should be concatenated and once the conversation has complete a single final message with the conversation analysis will be sent.

> :warning: **DEPRECATED**: This will be removed in a future release, please migrate away from it as soon as possible.

### Example Usage

<!-- UsageSnippet language="go" operationID="run_conversation_simulation_route_stream" method="post" path="/v1/convai/agents/{agent_id}/simulate-conversation/stream" -->
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

    res, err := s.AgentsPlatform.RunConversationSimulationRouteStream(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodySimulatesAConversationStreamV1ConvaiAgentsAgentIDSimulateConversationStreamPost{
        SimulationSpecification: components.ConversationSimulationSpecification{
            SimulatedUserConfig: components.AgentConfigAPIModelInput{
                FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
            },
        },
        ExtraEvaluationCriteria: []components.PromptEvaluationCriteria{
            components.PromptEvaluationCriteria{
                ID: "1234567890",
                Name: "Customer satisfaction check",
                ConversationGoalPrompt: "You are a helpful assistant that can answer questions about the topic of the conversation.",
            },
        },
    })
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
| `opts`                                                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                                                               | The options for this request.                                                                                                                                                                                    |                                                                                                                                                                                                                  |

### Response

**[*operations.RunConversationSimulationRouteStreamResponse](../../models/operations/runconversationsimulationroutestreamresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentTestFolder

Creates a folder for organizing agent tests.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_test_folder_route" method="post" path="/v1/convai/agent-testing/folders" -->
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

    res, err := s.AgentsPlatform.CreateAgentTestFolder(ctx, components.BodyCreateAgentTestFolderV1ConvaiAgentTestingFoldersPost{
        Name: "<value>",
    })
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
| `request`                                                                                                                                                  | [components.BodyCreateAgentTestFolderV1ConvaiAgentTestingFoldersPost](../../models/components/bodycreateagenttestfolderv1convaiagenttestingfolderspost.md) | :heavy_check_mark:                                                                                                                                         | The request object to use for the request.                                                                                                                 |
| `opts`                                                                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                                                                   | :heavy_minus_sign:                                                                                                                                         | The options for this request.                                                                                                                              |

### Response

**[*operations.CreateAgentTestFolderRouteResponse](../../models/operations/createagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentTestFolder

Gets an agent test folder by ID, including its folder path.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_test_folder_route" method="get" path="/v1/convai/agent-testing/folders/{folder_id}" -->
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

    res, err := s.AgentsPlatform.GetAgentTestFolder(ctx, "tfld_7301khxdkycse5f88fzjdtrterzm")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentTestFolderResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `folderID`                                               | `string`                                                 | :heavy_check_mark:                                       | The folder ID.                                           | tfld_7301khxdkycse5f88fzjdtrterzm                        |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetAgentTestFolderRouteResponse](../../models/operations/getagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateAgentTestFolder

Updates an agent test folder. Currently only supports updating the folder name.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_agent_test_folder_route" method="patch" path="/v1/convai/agent-testing/folders/{folder_id}" -->
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

    res, err := s.AgentsPlatform.UpdateAgentTestFolder(ctx, "tfld_7301khxdkycse5f88fzjdtrterzm", components.BodyUpdateAgentTestFolderV1ConvaiAgentTestingFoldersFolderIDPatch{
        Name: "<value>",
    })
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
| `opts`                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | The options for this request.                                                                                                                                                |                                                                                                                                                                              |

### Response

**[*operations.UpdateAgentTestFolderRouteResponse](../../models/operations/updateagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAgentTestFolder

Deletes an agent test folder by ID. Use force=true to delete a non-empty folder and all its contents.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_agent_test_folder_route" method="delete" path="/v1/convai/agent-testing/folders/{folder_id}" -->
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

    res, err := s.AgentsPlatform.DeleteAgentTestFolder(ctx, "tfld_7301khxdkycse5f88fzjdtrterzm", elevenlabsgo.Pointer(false))
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `folderID`                                               | `string`                                                 | :heavy_check_mark:                                       | The folder ID.                                           | tfld_7301khxdkycse5f88fzjdtrterzm                        |
| `force`                                                  | `*bool`                                                  | :heavy_minus_sign:                                       | Force delete. Required for deleting non-empty folders.   |                                                          |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteAgentTestFolderRouteResponse](../../models/operations/deleteagenttestfolderrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AgentTestingBulkMove

Moves multiple tests or folders from one folder to another.

### Example Usage

<!-- UsageSnippet language="go" operationID="agent_testing_bulk_move_route" method="post" path="/v1/convai/agent-testing/bulk-move" -->
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

    res, err := s.AgentsPlatform.AgentTestingBulkMove(ctx, components.BodyBulkMoveTestsToFolderV1ConvaiAgentTestingBulkMovePost{
        EntityIds: []string{
            "<value 1>",
            "<value 2>",
        },
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

| Parameter                                                                                                                                                    | Type                                                                                                                                                         | Required                                                                                                                                                     | Description                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                        | :heavy_check_mark:                                                                                                                                           | The context to use for the request.                                                                                                                          |
| `request`                                                                                                                                                    | [components.BodyBulkMoveTestsToFolderV1ConvaiAgentTestingBulkMovePost](../../models/components/bodybulkmoveteststofolderv1convaiagenttestingbulkmovepost.md) | :heavy_check_mark:                                                                                                                                           | The request object to use for the request.                                                                                                                   |
| `opts`                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                     | :heavy_minus_sign:                                                                                                                                           | The options for this request.                                                                                                                                |

### Response

**[*operations.AgentTestingBulkMoveRouteResponse](../../models/operations/agenttestingbulkmoverouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationHistories

Get all conversations of agents that user owns. With option to restrict to a specific agent.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_histories_route" method="get" path="/v1/convai/conversations" -->
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

    res, err := s.AgentsPlatform.GetConversationHistories(ctx, operations.GetConversationHistoriesRouteRequest{
        AgentID: elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"),
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

## GetConversationUsers

Get distinct users from conversations with pagination.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_users_route" method="get" path="/v1/convai/users" -->
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

    res, err := s.AgentsPlatform.GetConversationUsers(ctx, operations.GetConversationUsersRouteRequest{
        AgentID: elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"),
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

## GetConversationHistory

Get the details of a particular conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_history_route" method="get" path="/v1/convai/conversations/{conversation_id}" -->
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

    res, err := s.AgentsPlatform.GetConversationHistory(ctx, "21m00Tcm4TlvDq8ikWAM", operations.FormatJSON.ToPointer())
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                           | Type                                                                                                                                                | Required                                                                                                                                            | Description                                                                                                                                         | Example                                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                               | [context.Context](https://pkg.go.dev/context#Context)                                                                                               | :heavy_check_mark:                                                                                                                                  | The context to use for the request.                                                                                                                 |                                                                                                                                                     |
| `conversationID`                                                                                                                                    | `string`                                                                                                                                            | :heavy_check_mark:                                                                                                                                  | The id of the conversation you're taking the action on.                                                                                             | 21m00Tcm4TlvDq8ikWAM                                                                                                                                |
| `format`                                                                                                                                            | [*operations.Format](../../models/operations/format.md)                                                                                             | :heavy_minus_sign:                                                                                                                                  | Response format. Defaults to 'json'. Set to 'opentelemetry' for an OTLP-compatible trace payload using the same structure as the post-call webhook. |                                                                                                                                                     |
| `opts`                                                                                                                                              | [][operations.Option](../../models/operations/option.md)                                                                                            | :heavy_minus_sign:                                                                                                                                  | The options for this request.                                                                                                                       |                                                                                                                                                     |

### Response

**[*operations.GetConversationHistoryRouteResponse](../../models/operations/getconversationhistoryrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteConversation

Delete a particular conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_conversation_route" method="delete" path="/v1/convai/conversations/{conversation_id}" -->
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

    res, err := s.AgentsPlatform.DeleteConversation(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `conversationID`                                         | `string`                                                 | :heavy_check_mark:                                       | The id of the conversation you're taking the action on.  | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.DeleteConversationRouteResponse](../../models/operations/deleteconversationrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationSipMessages

Get SIP messages associated with a conversation's phone call

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_sip_messages" method="get" path="/v1/convai/conversations/{conversation_id}/sip-messages" -->
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

    res, err := s.AgentsPlatform.GetConversationSipMessages(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer[int64](20), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetSIPLogMessagesResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                        | Type                                                             | Required                                                         | Description                                                      | Example                                                          |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `ctx`                                                            | [context.Context](https://pkg.go.dev/context#Context)            | :heavy_check_mark:                                               | The context to use for the request.                              |                                                                  |
| `conversationID`                                                 | `string`                                                         | :heavy_check_mark:                                               | The id of the conversation you're taking the action on.          | 21m00Tcm4TlvDq8ikWAM                                             |
| `pageSize`                                                       | `*int64`                                                         | :heavy_minus_sign:                                               | N/A                                                              |                                                                  |
| `cursor`                                                         | `*string`                                                        | :heavy_minus_sign:                                               | Used for fetching next page. Cursor is returned in the response. |                                                                  |
| `opts`                                                           | [][operations.Option](../../models/operations/option.md)         | :heavy_minus_sign:                                               | The options for this request.                                    |                                                                  |

### Response

**[*operations.GetConversationSipMessagesResponse](../../models/operations/getconversationsipmessagesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationAudio

Get the audio recording of a particular conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_audio_route" method="get" path="/v1/convai/conversations/{conversation_id}/audio" -->
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

    res, err := s.AgentsPlatform.GetConversationAudio(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `conversationID`                                         | `string`                                                 | :heavy_check_mark:                                       | The id of the conversation you're taking the action on.  | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetConversationAudioRouteResponse](../../models/operations/getconversationaudiorouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## PostConversationFeedback

Send the feedback for the given conversation

### Example Usage

<!-- UsageSnippet language="go" operationID="post_conversation_feedback_route" method="post" path="/v1/convai/conversations/{conversation_id}/feedback" -->
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

    res, err := s.AgentsPlatform.PostConversationFeedback(ctx, "21m00Tcm4TlvDq8ikWAM", components.ConversationFeedbackRequestModel{
        Feedback: components.UserFeedbackScoreLike.ToPointer(),
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

## TextSearchConversationMessages

Search through conversation transcript messages by full-text and fuzzy search

### Example Usage

<!-- UsageSnippet language="go" operationID="text_search_conversation_messages_route" method="get" path="/v1/convai/conversations/messages/text-search" example="default" -->
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

    res, err := s.AgentsPlatform.TextSearchConversationMessages(ctx, operations.TextSearchConversationMessagesRouteRequest{
        TextQuery: "refund policy",
        AgentID: elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"),
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

## SmartSearchConversationMessages

Search conversation transcripts by semantic similarity to surface relevant messages based on meaning and intent, rather than exact keyword matches

### Example Usage

<!-- UsageSnippet language="go" operationID="smart_search_conversation_messages_route" method="get" path="/v1/convai/conversations/messages/smart-search" example="default" -->
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

    res, err := s.AgentsPlatform.SmartSearchConversationMessages(ctx, "Customer asking to cancel and get money back", elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"), elevenlabsgo.Pointer[int64](20), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.MessagesSearchResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            | Example                                                                                                |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |                                                                                                        |
| `textQuery`                                                                                            | `string`                                                                                               | :heavy_check_mark:                                                                                     | The search query text for semantic similarity matching                                                 |                                                                                                        |
| `agentID`                                                                                              | `*string`                                                                                              | :heavy_minus_sign:                                                                                     | Agent id (agent_…) or speech engine external id (seng_), resolved to the same underlying resource.     | **Example 1:** agent_3701k3ttaq12ewp8b7qv5rfyszkz<br/>**Example 2:** seng_3701k3ttaq12ewp8b7qv5rfyszkz |
| `pageSize`                                                                                             | `*int64`                                                                                               | :heavy_minus_sign:                                                                                     | Number of results per page. Max 50.                                                                    |                                                                                                        |
| `cursor`                                                                                               | `*string`                                                                                              | :heavy_minus_sign:                                                                                     | Used for fetching next page. Cursor is returned in the response.                                       |                                                                                                        |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |                                                                                                        |

### Response

**[*operations.SmartSearchConversationMessagesRouteResponse](../../models/operations/smartsearchconversationmessagesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AssignConversationTagsRoute

Assign one or more conversation tags to a conversation. Tags that are already assigned are ignored. Tags must belong to the same workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="assign_conversation_tags_route" method="post" path="/v1/convai/conversations/{conversation_id}/tags" -->
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

    res, err := s.AgentsPlatform.AssignConversationTagsRoute(ctx, "<id>", components.AssignConversationTagsRequestModel{
        TagIds: []string{},
    })
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                      | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                          | :heavy_check_mark:                                                                                             | The context to use for the request.                                                                            |
| `conversationID`                                                                                               | `string`                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `body`                                                                                                         | [components.AssignConversationTagsRequestModel](../../models/components/assignconversationtagsrequestmodel.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `opts`                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                       | :heavy_minus_sign:                                                                                             | The options for this request.                                                                                  |

### Response

**[*operations.AssignConversationTagsRouteResponse](../../models/operations/assignconversationtagsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UnassignConversationTagRoute

Remove a single conversation tag from a conversation.

### Example Usage

<!-- UsageSnippet language="go" operationID="unassign_conversation_tag_route" method="delete" path="/v1/convai/conversations/{conversation_id}/tags/{tag_id}" -->
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

    res, err := s.AgentsPlatform.UnassignConversationTagRoute(ctx, "<id>", "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `conversationID`                                         | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `tagID`                                                  | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.UnassignConversationTagRouteResponse](../../models/operations/unassignconversationtagrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListConversationTagsRoute

List conversation tags for the workspace, ordered by most recently created first.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_conversation_tags_route" method="get" path="/v1/convai/tags" -->
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

    res, err := s.AgentsPlatform.ListConversationTagsRoute(ctx, elevenlabsgo.Pointer[int64](100), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConversationTagsPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                        | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `ctx`                                                            | [context.Context](https://pkg.go.dev/context#Context)            | :heavy_check_mark:                                               | The context to use for the request.                              |
| `pageSize`                                                       | `*int64`                                                         | :heavy_minus_sign:                                               | How many conversation tags to return. Can not exceed 100.        |
| `cursor`                                                         | `*string`                                                        | :heavy_minus_sign:                                               | Used for fetching next page. Cursor is returned in the response. |
| `opts`                                                           | [][operations.Option](../../models/operations/option.md)         | :heavy_minus_sign:                                               | The options for this request.                                    |

### Response

**[*operations.ListConversationTagsRouteResponse](../../models/operations/listconversationtagsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateConversationTagRoute

Create a new conversation tag for the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_conversation_tag_route" method="post" path="/v1/convai/tags" -->
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

    res, err := s.AgentsPlatform.CreateConversationTagRoute(ctx, components.CreateConversationTagRequestModel{
        Title: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationTagResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                    | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                        | :heavy_check_mark:                                                                                           | The context to use for the request.                                                                          |
| `request`                                                                                                    | [components.CreateConversationTagRequestModel](../../models/components/createconversationtagrequestmodel.md) | :heavy_check_mark:                                                                                           | The request object to use for the request.                                                                   |
| `opts`                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                     | :heavy_minus_sign:                                                                                           | The options for this request.                                                                                |

### Response

**[*operations.CreateConversationTagRouteResponse](../../models/operations/createconversationtagrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetConversationTagRoute

Get a conversation tag by ID.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_conversation_tag_route" method="get" path="/v1/convai/tags/{tag_id}" -->
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

    res, err := s.AgentsPlatform.GetConversationTagRoute(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationTagResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `tagID`                                                  | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetConversationTagRouteResponse](../../models/operations/getconversationtagrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteConversationTagRoute

Delete a conversation tag. Restricted to the tag owner or a workspace admin.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_conversation_tag_route" method="delete" path="/v1/convai/tags/{tag_id}" -->
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

    res, err := s.AgentsPlatform.DeleteConversationTagRoute(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `tagID`                                                  | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.DeleteConversationTagRouteResponse](../../models/operations/deleteconversationtagrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateConversationTagRoute

Update a conversation tag's title and/or description. Restricted to the tag owner or a workspace admin.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_conversation_tag_route" method="patch" path="/v1/convai/tags/{tag_id}" -->
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

    res, err := s.AgentsPlatform.UpdateConversationTagRoute(ctx, "<id>", components.PatchConversationTagRequestModel{})
    if err != nil {
        log.Fatal(err)
    }
    if res.ConversationTagResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `tagID`                                                                                                    | `string`                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `body`                                                                                                     | [components.PatchConversationTagRequestModel](../../models/components/patchconversationtagrequestmodel.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

### Response

**[*operations.UpdateConversationTagRouteResponse](../../models/operations/updateconversationtagrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreatePhoneNumber

Import Phone Number from provider configuration (Twilio, Exotel, or SIP trunk)

### Example Usage

<!-- UsageSnippet language="go" operationID="create_phone_number_route" method="post" path="/v1/convai/phone-numbers" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/models/operations"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.CreatePhoneNumber(ctx, operations.CreatePhoneRequestCreateExotelPhoneNumberRequest(
        components.CreateExotelPhoneNumberRequest{
            PhoneNumber: "+919999999999",
            Label: "Exotel Outbound",
            AccountSid: "your-account-sid",
            APIKey: "your-api-key",
            APIToken: "********",
            APISubdomain: components.ExotelAPISubdomainAPIInExotelCom,
            AppID: "12345",
        },
    ))
    if err != nil {
        log.Fatal(err)
    }
    if res.CreatePhoneNumberResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                          | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `ctx`                                                              | [context.Context](https://pkg.go.dev/context#Context)              | :heavy_check_mark:                                                 | The context to use for the request.                                |
| `request`                                                          | [operations.PhoneRequest](../../models/operations/phonerequest.md) | :heavy_check_mark:                                                 | The request object to use for the request.                         |
| `opts`                                                             | [][operations.Option](../../models/operations/option.md)           | :heavy_minus_sign:                                                 | The options for this request.                                      |

### Response

**[*operations.CreatePhoneNumberRouteResponse](../../models/operations/createphonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListPhoneNumbers

Retrieve all Phone Numbers

### Example Usage

<!-- UsageSnippet language="go" operationID="list_phone_numbers_route" method="get" path="/v1/convai/phone-numbers" -->
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

    res, err := s.AgentsPlatform.ListPhoneNumbers(ctx, nil, nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseListPhoneNumbersV1ConvaiPhoneNumbersGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `ctx`                                                                         | [context.Context](https://pkg.go.dev/context#Context)                         | :heavy_check_mark:                                                            | The context to use for the request.                                           |
| `provider`                                                                    | [*components.TelephonyProvider](../../models/components/telephonyprovider.md) | :heavy_minus_sign:                                                            | Filter by telephony provider                                                  |
| `agentID`                                                                     | `*string`                                                                     | :heavy_minus_sign:                                                            | Filter by assigned agent ID                                                   |
| `branchID`                                                                    | `*string`                                                                     | :heavy_minus_sign:                                                            | Filter by assigned branch ID                                                  |
| `opts`                                                                        | [][operations.Option](../../models/operations/option.md)                      | :heavy_minus_sign:                                                            | The options for this request.                                                 |

### Response

**[*operations.ListPhoneNumbersRouteResponse](../../models/operations/listphonenumbersrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetPhoneNumber

Retrieve Phone Number details by ID

### Example Usage

<!-- UsageSnippet language="go" operationID="get_phone_number_route" method="get" path="/v1/convai/phone-numbers/{phone_number_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetPhoneNumber(ctx, "TeaqRRdTcIfIu2i7BYfT")
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet != nil {
        switch res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.Type {
            case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeTwilio:
                // res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberTwilioResponseModel is populated
            case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeExotel:
                // res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberExotelResponseModel is populated
            case operations.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGetTypeSipTrunk:
                // res.ResponseGetPhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDGet.GetPhoneNumberSIPTrunkResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `ctx`                                                                  | [context.Context](https://pkg.go.dev/context#Context)                  | :heavy_check_mark:                                                     | The context to use for the request.                                    |                                                                        |
| `phoneNumberID`                                                        | `string`                                                               | :heavy_check_mark:                                                     | The phone number ID. This is returned when a phone number is imported. | TeaqRRdTcIfIu2i7BYfT                                                   |
| `opts`                                                                 | [][operations.Option](../../models/operations/option.md)               | :heavy_minus_sign:                                                     | The options for this request.                                          |                                                                        |

### Response

**[*operations.GetPhoneNumberRouteResponse](../../models/operations/getphonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeletePhoneNumber

Delete Phone Number by ID

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_phone_number_route" method="delete" path="/v1/convai/phone-numbers/{phone_number_id}" -->
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

    res, err := s.AgentsPlatform.DeletePhoneNumber(ctx, "TeaqRRdTcIfIu2i7BYfT")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `ctx`                                                                  | [context.Context](https://pkg.go.dev/context#Context)                  | :heavy_check_mark:                                                     | The context to use for the request.                                    |                                                                        |
| `phoneNumberID`                                                        | `string`                                                               | :heavy_check_mark:                                                     | The phone number ID. This is returned when a phone number is imported. | TeaqRRdTcIfIu2i7BYfT                                                   |
| `opts`                                                                 | [][operations.Option](../../models/operations/option.md)               | :heavy_minus_sign:                                                     | The options for this request.                                          |                                                                        |

### Response

**[*operations.DeletePhoneNumberRouteResponse](../../models/operations/deletephonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdatePhoneNumber

Update assigned agent of a phone number

### Example Usage

<!-- UsageSnippet language="go" operationID="update_phone_number_route" method="patch" path="/v1/convai/phone-numbers/{phone_number_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.UpdatePhoneNumber(ctx, "TeaqRRdTcIfIu2i7BYfT", components.UpdatePhoneNumberRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch != nil {
        switch res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.Type {
            case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeTwilio:
                // res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberTwilioResponseModel is populated
            case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeExotel:
                // res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberExotelResponseModel is populated
            case operations.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatchTypeSipTrunk:
                // res.ResponseUpdatePhoneNumberV1ConvaiPhoneNumbersPhoneNumberIDPatch.GetPhoneNumberSIPTrunkResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                  | Type                                                                                       | Required                                                                                   | Description                                                                                | Example                                                                                    |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `ctx`                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                      | :heavy_check_mark:                                                                         | The context to use for the request.                                                        |                                                                                            |
| `phoneNumberID`                                                                            | `string`                                                                                   | :heavy_check_mark:                                                                         | The phone number ID. This is returned when a phone number is imported.                     | TeaqRRdTcIfIu2i7BYfT                                                                       |
| `body`                                                                                     | [components.UpdatePhoneNumberRequest](../../models/components/updatephonenumberrequest.md) | :heavy_check_mark:                                                                         | N/A                                                                                        |                                                                                            |
| `opts`                                                                                     | [][operations.Option](../../models/operations/option.md)                                   | :heavy_minus_sign:                                                                         | The options for this request.                                                              |                                                                                            |

### Response

**[*operations.UpdatePhoneNumberRouteResponse](../../models/operations/updatephonenumberrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListSipMessages

Get SIP messages for a phone number

### Example Usage

<!-- UsageSnippet language="go" operationID="list_sip_messages" method="get" path="/v1/convai/phone-numbers/{phone_number_id}/sip-messages" -->
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

    res, err := s.AgentsPlatform.ListSipMessages(ctx, "TeaqRRdTcIfIu2i7BYfT", elevenlabsgo.Pointer[int64](20), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetSIPLogMessagesResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            | Example                                                                |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `ctx`                                                                  | [context.Context](https://pkg.go.dev/context#Context)                  | :heavy_check_mark:                                                     | The context to use for the request.                                    |                                                                        |
| `phoneNumberID`                                                        | `string`                                                               | :heavy_check_mark:                                                     | The phone number ID. This is returned when a phone number is imported. | TeaqRRdTcIfIu2i7BYfT                                                   |
| `pageSize`                                                             | `*int64`                                                               | :heavy_minus_sign:                                                     | N/A                                                                    |                                                                        |
| `cursor`                                                               | `*string`                                                              | :heavy_minus_sign:                                                     | Used for fetching next page. Cursor is returned in the response.       |                                                                        |
| `opts`                                                                 | [][operations.Option](../../models/operations/option.md)               | :heavy_minus_sign:                                                     | The options for this request.                                          |                                                                        |

### Response

**[*operations.ListSipMessagesResponse](../../models/operations/listsipmessagesresponse.md), error**

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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.ListAvailableLlms(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.LLMListResponseModelInput != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.ListAvailableLlmsResponse](../../models/operations/listavailablellmsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UploadFile

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.UploadFile(ctx, "<id>", components.BodyUploadFileV1ConvaiConversationsConversationIDFilesPost{
        File: components.BodyUploadFileV1ConvaiConversationsConversationIDFilesPostFile{
            FileName: "example.file",
            Content: example,
        },
    })
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
| `opts`                                                                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                                                                       | :heavy_minus_sign:                                                                                                                                             | The options for this request.                                                                                                                                  |

### Response

**[*operations.UploadFileRouteResponse](../../models/operations/uploadfilerouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CancelFileUpload

Remove a file upload from a conversation. Only possible if the file hasn't already been used in the conversation.

### Example Usage

<!-- UsageSnippet language="go" operationID="cancel_file_upload_route" method="delete" path="/v1/convai/conversations/{conversation_id}/files/{file_id}" -->
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

    res, err := s.AgentsPlatform.CancelFileUpload(ctx, "<id>", "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.ConvAIFileUploadResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `fileID`                                                 | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `conversationID`                                         | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetLiveCount(ctx, elevenlabsgo.Pointer("21m00Tcm4TlvDq8ikWAM"))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetLiveCountResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `*string`                                                | :heavy_minus_sign:                                       | The id of an agent to restrict the analytics to.         | 21m00Tcm4TlvDq8ikWAM                                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetLiveCountResponse](../../models/operations/getlivecountresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentKnowledgeBaseSummaries

Gets multiple knowledge base document summaries by their IDs.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_knowledge_base_summaries_route" method="get" path="/v1/convai/knowledge-base/summaries" -->
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

    res, err := s.AgentsPlatform.GetAgentKnowledgeBaseSummaries(ctx, []string{
        "21m00Tcm4TlvDq8ikWAM",
        "31n11Udm5UmwEr9jkXBN",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseGetKnowledgeBaseSummariesByIdsV1ConvaiKnowledgeBaseSummariesGet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `documentIds`                                            | []`string`                                               | :heavy_check_mark:                                       | The ids of knowledge base documents.                     | [<br/>"21m00Tcm4TlvDq8ikWAM",<br/>"31n11Udm5UmwEr9jkXBN"<br/>] |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetAgentKnowledgeBaseSummariesRouteResponse](../../models/operations/getagentknowledgebasesummariesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetKnowledgeBaseList

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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetKnowledgeBaseList(ctx, operations.GetKnowledgeBaseListRouteRequest{})
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.AddDocumentationToKnowledgeBase(ctx, elevenlabsgo.Pointer(""), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.AddKnowledgeBaseResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                 | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                     | [context.Context](https://pkg.go.dev/context#Context)                                                                                     | :heavy_check_mark:                                                                                                                        | The context to use for the request.                                                                                                       |
| `agentID`                                                                                                                                 | `*string`                                                                                                                                 | :heavy_minus_sign:                                                                                                                        | N/A                                                                                                                                       |
| `body`                                                                                                                                    | [*components.BodyAddToKnowledgeBaseV1ConvaiKnowledgeBasePost](../../models/components/bodyaddtoknowledgebasev1convaiknowledgebasepost.md) | :heavy_minus_sign:                                                                                                                        | N/A                                                                                                                                       |
| `opts`                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                  | :heavy_minus_sign:                                                                                                                        | The options for this request.                                                                                                             |

### Response

**[*operations.AddDocumentationToKnowledgeBaseResponse](../../models/operations/adddocumentationtoknowledgebaseresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateURLDocument

Create a knowledge base document generated by scraping the given webpage.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_url_document_route" method="post" path="/v1/convai/knowledge-base/url" -->
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

    res, err := s.AgentsPlatform.CreateURLDocument(ctx, components.BodyCreateURLDocumentV1ConvaiKnowledgeBaseURLPost{
        URL: "https://clueless-marketplace.biz/",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddKnowledgeBaseResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                    | Type                                                                                                                                         | Required                                                                                                                                     | Description                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                        | :heavy_check_mark:                                                                                                                           | The context to use for the request.                                                                                                          |
| `request`                                                                                                                                    | [components.BodyCreateURLDocumentV1ConvaiKnowledgeBaseURLPost](../../models/components/bodycreateurldocumentv1convaiknowledgebaseurlpost.md) | :heavy_check_mark:                                                                                                                           | The request object to use for the request.                                                                                                   |
| `opts`                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                     | :heavy_minus_sign:                                                                                                                           | The options for this request.                                                                                                                |

### Response

**[*operations.CreateURLDocumentRouteResponse](../../models/operations/createurldocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateFileDocument

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.CreateFileDocument(ctx, components.BodyCreateFileDocumentV1ConvaiKnowledgeBaseFilePost{
        File: components.BodyCreateFileDocumentV1ConvaiKnowledgeBaseFilePostFile{
            FileName: "example.file",
            Content: example,
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddKnowledgeBaseResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                        | Type                                                                                                                                             | Required                                                                                                                                         | Description                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                            | :heavy_check_mark:                                                                                                                               | The context to use for the request.                                                                                                              |
| `request`                                                                                                                                        | [components.BodyCreateFileDocumentV1ConvaiKnowledgeBaseFilePost](../../models/components/bodycreatefiledocumentv1convaiknowledgebasefilepost.md) | :heavy_check_mark:                                                                                                                               | The request object to use for the request.                                                                                                       |
| `opts`                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                         | :heavy_minus_sign:                                                                                                                               | The options for this request.                                                                                                                    |

### Response

**[*operations.CreateFileDocumentRouteResponse](../../models/operations/createfiledocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateTextDocument

Create a knowledge base document containing the provided text.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_text_document_route" method="post" path="/v1/convai/knowledge-base/text" -->
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

    res, err := s.AgentsPlatform.CreateTextDocument(ctx, components.BodyCreateTextDocumentV1ConvaiKnowledgeBaseTextPost{
        Text: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.AddKnowledgeBaseResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                        | Type                                                                                                                                             | Required                                                                                                                                         | Description                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                            | :heavy_check_mark:                                                                                                                               | The context to use for the request.                                                                                                              |
| `request`                                                                                                                                        | [components.BodyCreateTextDocumentV1ConvaiKnowledgeBaseTextPost](../../models/components/bodycreatetextdocumentv1convaiknowledgebasetextpost.md) | :heavy_check_mark:                                                                                                                               | The request object to use for the request.                                                                                                       |
| `opts`                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                         | :heavy_minus_sign:                                                                                                                               | The options for this request.                                                                                                                    |

### Response

**[*operations.CreateTextDocumentRouteResponse](../../models/operations/createtextdocumentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateDocument

Update the name and/or content of a document.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_document_route" method="patch" path="/v1/convai/knowledge-base/{documentation_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.UpdateDocument(ctx, "21m00Tcm4TlvDq8ikWAM", &components.BodyUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch{
        Name: elevenlabsgo.Pointer("<value>"),
    })
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
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                         | Type                                                                                                                                                              | Required                                                                                                                                                          | Description                                                                                                                                                       | Example                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                             | [context.Context](https://pkg.go.dev/context#Context)                                                                                                             | :heavy_check_mark:                                                                                                                                                | The context to use for the request.                                                                                                                               |                                                                                                                                                                   |
| `documentationID`                                                                                                                                                 | `string`                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                | The id of a document from the knowledge base. This is returned on document addition.                                                                              | 21m00Tcm4TlvDq8ikWAM                                                                                                                                              |
| `body`                                                                                                                                                            | [*components.BodyUpdateDocumentV1ConvaiKnowledgeBaseDocumentationIDPatch](../../models/components/bodyupdatedocumentv1convaiknowledgebasedocumentationidpatch.md) | :heavy_minus_sign:                                                                                                                                                | N/A                                                                                                                                                               |                                                                                                                                                                   |
| `opts`                                                                                                                                                            | [][operations.Option](../../models/operations/option.md)                                                                                                          | :heavy_minus_sign:                                                                                                                                                | The options for this request.                                                                                                                                     |                                                                                                                                                                   |

### Response

**[*operations.UpdateDocumentRouteResponse](../../models/operations/updatedocumentrouteresponse.md), error**

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
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetDocumentationFromKnowledgeBase(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(""))
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
        }

    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `agentID`                                                                            | `*string`                                                                            | :heavy_minus_sign:                                                                   | N/A                                                                                  |                                                                                      |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.DeleteKnowledgeBaseDocument(ctx, "21m00Tcm4TlvDq8ikWAM", elevenlabsgo.Pointer(false))
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
| `opts`                                                                                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                                                                    | The options for this request.                                                                                                                                                                                                         |                                                                                                                                                                                                                                       |

### Response

**[*operations.DeleteKnowledgeBaseDocumentResponse](../../models/operations/deleteknowledgebasedocumentresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateFileDocumentRoute

Update the source file of a file document. The document name, content, and metadata are updated to reflect the new file. Any manual content edits will be overwritten.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_file_document_route" method="patch" path="/v1/convai/knowledge-base/{documentation_id}/update-file" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"os"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    example, fileErr := os.Open("example.file")
    if fileErr != nil {
        panic(fileErr)
    }

    res, err := s.AgentsPlatform.UpdateFileDocumentRoute(ctx, "21m00Tcm4TlvDq8ikWAM", components.BodyUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch{
        File: components.BodyUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatchFile{
            FileName: "example.file",
            Content: example,
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch != nil {
        switch res.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch.Type {
            case operations.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatchTypeURLObj:
                // res.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch.GetKnowledgeBaseURLResponseModel is populated
            case operations.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatchTypeFile:
                // res.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch.GetKnowledgeBaseFileResponseModel is populated
            case operations.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatchTypeText:
                // res.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch.GetKnowledgeBaseTextResponseModel is populated
            case operations.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatchTypeFolder:
                // res.ResponseUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch.GetKnowledgeBaseFolderResponseModel is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                                                                                                                    | Type                                                                                                                                                                                         | Required                                                                                                                                                                                     | Description                                                                                                                                                                                  | Example                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                           | The context to use for the request.                                                                                                                                                          |                                                                                                                                                                                              |
| `documentationID`                                                                                                                                                                            | `string`                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                           | The id of a document from the knowledge base. This is returned on document addition.                                                                                                         | 21m00Tcm4TlvDq8ikWAM                                                                                                                                                                         |
| `body`                                                                                                                                                                                       | [components.BodyUpdateFileDocumentV1ConvaiKnowledgeBaseDocumentationIDUpdateFilePatch](../../models/components/bodyupdatefiledocumentv1convaiknowledgebasedocumentationidupdatefilepatch.md) | :heavy_check_mark:                                                                                                                                                                           | N/A                                                                                                                                                                                          |                                                                                                                                                                                              |
| `opts`                                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                                           | The options for this request.                                                                                                                                                                |                                                                                                                                                                                              |

### Response

**[*operations.UpdateFileDocumentRouteResponse](../../models/operations/updatefiledocumentrouteresponse.md), error**

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetRagIndexOverview(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGIndexOverviewResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetOrCreateRagIndexes(ctx, components.BodyComputeRAGIndexesInBatchV1ConvaiKnowledgeBaseRAGIndexPost{
        Items: []components.GetOrCreateRAGIndexRequestModel{
            components.GetOrCreateRAGIndexRequestModel{
                DocumentID: "<id>",
                CreateIfMissing: false,
            },
        },
    })
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
| `request`                                                                                                                                                            | [components.BodyComputeRAGIndexesInBatchV1ConvaiKnowledgeBaseRAGIndexPost](../../models/components/bodycomputeragindexesinbatchv1convaiknowledgebaseragindexpost.md) | :heavy_check_mark:                                                                                                                                                   | The request object to use for the request.                                                                                                                           |
| `opts`                                                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                                                             | :heavy_minus_sign:                                                                                                                                                   | The options for this request.                                                                                                                                        |

### Response

**[*operations.GetOrCreateRagIndexesResponse](../../models/operations/getorcreateragindexesresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RefreshURLDocument

Manually refresh a URL document by re-fetching its content from the source URL.

### Example Usage

<!-- UsageSnippet language="go" operationID="refresh_url_document_route" method="post" path="/v1/convai/knowledge-base/{documentation_id}/refresh" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/operations"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.RefreshURLDocument(ctx, "21m00Tcm4TlvDq8ikWAM")
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
        }

    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetRagIndexes(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGDocumentIndexesResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.RagIndexStatus(ctx, "21m00Tcm4TlvDq8ikWAM", components.RAGIndexRequestModel{})
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGDocumentIndexResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `body`                                                                               | [components.RAGIndexRequestModel](../../models/components/ragindexrequestmodel.md)   | :heavy_check_mark:                                                                   | N/A                                                                                  |                                                                                      |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.DeleteRagIndex(ctx, "21m00Tcm4TlvDq8ikWAM", "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.RAGDocumentIndexResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `ragIndexID`                                                                         | `string`                                                                             | :heavy_check_mark:                                                                   | The id of RAG index of document from the knowledge base.                             | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

### Response

**[*operations.DeleteRagIndexResponse](../../models/operations/deleteragindexresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## SearchKnowledgeBaseContent

Fuzzy text search over knowledge base document content

### Example Usage

<!-- UsageSnippet language="go" operationID="search_knowledge_base_content_route" method="get" path="/v1/convai/knowledge-base/search" -->
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

    res, err := s.AgentsPlatform.SearchKnowledgeBaseContent(ctx, "<value>", elevenlabsgo.Pointer[int64](30), nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseContentSearchResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                      | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `ctx`                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                          | :heavy_check_mark:                                                                             | The context to use for the request.                                                            |
| `query`                                                                                        | `string`                                                                                       | :heavy_check_mark:                                                                             | The search query text                                                                          |
| `pageSize`                                                                                     | `*int64`                                                                                       | :heavy_minus_sign:                                                                             | How many documents to return at maximum. Can not exceed 100, defaults to 30.                   |
| `types`                                                                                        | [][components.KnowledgeBaseDocumentType](../../models/components/knowledgebasedocumenttype.md) | :heavy_minus_sign:                                                                             | If present, the endpoint will return only documents of the given types.                        |
| `cursor`                                                                                       | `*string`                                                                                      | :heavy_minus_sign:                                                                             | Used for fetching next page. Cursor is returned in the response.                               |
| `opts`                                                                                         | [][operations.Option](../../models/operations/option.md)                                       | :heavy_minus_sign:                                                                             | The options for this request.                                                                  |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetKnowledgeBaseDependentAgents(ctx, "21m00Tcm4TlvDq8ikWAM", nil, elevenlabsgo.Pointer[int64](30), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetKnowledgeBaseDependentAgentsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                       | Type                                                                                            | Required                                                                                        | Description                                                                                     | Example                                                                                         |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `ctx`                                                                                           | [context.Context](https://pkg.go.dev/context#Context)                                           | :heavy_check_mark:                                                                              | The context to use for the request.                                                             |                                                                                                 |
| `documentationID`                                                                               | `string`                                                                                        | :heavy_check_mark:                                                                              | The id of a document from the knowledge base. This is returned on document addition.            | 21m00Tcm4TlvDq8ikWAM                                                                            |
| `dependentType`                                                                                 | [*components.KnowledgeBaseDependentType](../../models/components/knowledgebasedependenttype.md) | :heavy_minus_sign:                                                                              | Type of dependent agents to return.                                                             |                                                                                                 |
| `pageSize`                                                                                      | `*int64`                                                                                        | :heavy_minus_sign:                                                                              | How many documents to return at maximum. Can not exceed 100, defaults to 30.                    |                                                                                                 |
| `cursor`                                                                                        | `*string`                                                                                       | :heavy_minus_sign:                                                                              | Used for fetching next page. Cursor is returned in the response.                                |                                                                                                 |
| `opts`                                                                                          | [][operations.Option](../../models/operations/option.md)                                        | :heavy_minus_sign:                                                                              | The options for this request.                                                                   |                                                                                                 |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetKnowledgeBaseContent(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.Res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetKnowledgeBaseSourceFileURL(ctx, "21m00Tcm4TlvDq8ikWAM")
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseSourceFileURLResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetDocumentationChunkFromKnowledgeBase(ctx, "21m00Tcm4TlvDq8ikWAM", "1", components.EmbeddingModelEnumE5Mistral7bInstruct.ToPointer())
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseDocumentChunkResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `chunkID`                                                                            | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document RAG chunk from the knowledge base.                              | 1                                                                                    |
| `embeddingModel`                                                                     | [*components.EmbeddingModelEnum](../../models/components/embeddingmodelenum.md)      | :heavy_minus_sign:                                                                   | The embedding model used to retrieve the chunk.                                      |                                                                                      |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

### Response

**[*operations.GetDocumentationChunkFromKnowledgeBaseResponse](../../models/operations/getdocumentationchunkfromknowledgebaseresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetDocumentationChunksFromKnowledgeBase

Get all RAG chunks for a specific knowledge base document.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_documentation_chunks_from_knowledge_base" method="get" path="/v1/convai/knowledge-base/{documentation_id}/chunks" -->
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

    res, err := s.AgentsPlatform.GetDocumentationChunksFromKnowledgeBase(ctx, "21m00Tcm4TlvDq8ikWAM", components.EmbeddingModelEnumE5Mistral7bInstruct, elevenlabsgo.Pointer[int64](30), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.KnowledgeBaseDocumentChunksResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |                                                                                      |
| `documentationID`                                                                    | `string`                                                                             | :heavy_check_mark:                                                                   | The id of a document from the knowledge base. This is returned on document addition. | 21m00Tcm4TlvDq8ikWAM                                                                 |
| `embeddingModel`                                                                     | [components.EmbeddingModelEnum](../../models/components/embeddingmodelenum.md)       | :heavy_check_mark:                                                                   | The embedding model used to retrieve the chunk.                                      |                                                                                      |
| `pageSize`                                                                           | `*int64`                                                                             | :heavy_minus_sign:                                                                   | How many documents to return at maximum. Can not exceed 100, defaults to 30.         |                                                                                      |
| `cursor`                                                                             | `*string`                                                                            | :heavy_minus_sign:                                                                   | Used for fetching next page. Cursor is returned in the response.                     |                                                                                      |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |                                                                                      |

### Response

**[*operations.GetDocumentationChunksFromKnowledgeBaseResponse](../../models/operations/getdocumentationchunksfromknowledgebaseresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetAgentTopicsRoute

Returns the latest topic discovery run results for a given agent.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_agent_topics_route" method="get" path="/v1/convai/agents/{agent_id}/topics" -->
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

    res, err := s.AgentsPlatform.GetAgentTopicsRoute(ctx, "<id>", nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetAgentTopicsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `agentID`                                                                                                                | `string`                                                                                                                 | :heavy_check_mark:                                                                                                       | ID of the agent                                                                                                          |
| `fromUnixSecs`                                                                                                           | `*int64`                                                                                                                 | :heavy_minus_sign:                                                                                                       | Start of the window to view topics for. When set with to_unix_secs, per-day topics in the range are aggregated together. |
| `toUnixSecs`                                                                                                             | `*int64`                                                                                                                 | :heavy_minus_sign:                                                                                                       | End of the window to view topics for.                                                                                    |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.GetAgentTopicsRouteResponse](../../models/operations/getagenttopicsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddTool

Add a new tool to the available tools in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_tool_route" method="post" path="/v1/convai/tools" -->
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

    res, err := s.AgentsPlatform.AddTool(ctx, components.ToolRequestModel{
        ToolConfig: components.CreateToolRequestModelToolConfigClient(
            components.ClientToolConfigInput{
                Name: "<value>",
                Description: "meh smuggle athwart yahoo whoa rapid interestingly ugh",
            },
        ),
    })
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
        }

    }
}
```

### Parameters

| Parameter                                                                  | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `ctx`                                                                      | [context.Context](https://pkg.go.dev/context#Context)                      | :heavy_check_mark:                                                         | The context to use for the request.                                        |
| `request`                                                                  | [components.ToolRequestModel](../../models/components/toolrequestmodel.md) | :heavy_check_mark:                                                         | The request object to use for the request.                                 |
| `opts`                                                                     | [][operations.Option](../../models/operations/option.md)                   | :heavy_minus_sign:                                                         | The options for this request.                                              |

### Response

**[*operations.AddToolRouteResponse](../../models/operations/addtoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetTools

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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetTools(ctx, operations.GetToolsRouteRequest{})
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

## GetTool

Get tool that is available in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_tool_route" method="get" path="/v1/convai/tools/{tool_id}" -->
```go
package main

import(
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
	"github.com/bdlilley/elevenlabs-go/models/components"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetTool(ctx, "<id>")
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
        }

    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `toolID`                                                 | `string`                                                 | :heavy_check_mark:                                       | ID of the requested tool.                                |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetToolRouteResponse](../../models/operations/gettoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateTool

Update tool that is available in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_tool_route" method="patch" path="/v1/convai/tools/{tool_id}" -->
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

    res, err := s.AgentsPlatform.UpdateTool(ctx, "<id>", components.ToolRequestModel{
        ToolConfig: components.CreateToolRequestModelToolConfigClient(
            components.ClientToolConfigInput{
                Name: "<value>",
                Description: "oh well-lit but underneath against uh-huh rationalise quicker",
            },
        ),
    })
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
        }

    }
}
```

### Parameters

| Parameter                                                                  | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `ctx`                                                                      | [context.Context](https://pkg.go.dev/context#Context)                      | :heavy_check_mark:                                                         | The context to use for the request.                                        |
| `toolID`                                                                   | `string`                                                                   | :heavy_check_mark:                                                         | ID of the requested tool.                                                  |
| `body`                                                                     | [components.ToolRequestModel](../../models/components/toolrequestmodel.md) | :heavy_check_mark:                                                         | N/A                                                                        |
| `opts`                                                                     | [][operations.Option](../../models/operations/option.md)                   | :heavy_minus_sign:                                                         | The options for this request.                                              |

### Response

**[*operations.UpdateToolRouteResponse](../../models/operations/updatetoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteTool

Delete tool from the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_tool_route" method="delete" path="/v1/convai/tools/{tool_id}" -->
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

    res, err := s.AgentsPlatform.DeleteTool(ctx, "<id>", elevenlabsgo.Pointer(false))
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                              | Type                                                                                                                                                   | Required                                                                                                                                               | Description                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                                                                  | :heavy_check_mark:                                                                                                                                     | The context to use for the request.                                                                                                                    |
| `toolID`                                                                                                                                               | `string`                                                                                                                                               | :heavy_check_mark:                                                                                                                                     | ID of the requested tool.                                                                                                                              |
| `force`                                                                                                                                                | `*bool`                                                                                                                                                | :heavy_minus_sign:                                                                                                                                     | If set to true, the tool will be deleted regardless of whether it is used by any agents and it will be removed from the dependent agents and branches. |
| `opts`                                                                                                                                                 | [][operations.Option](../../models/operations/option.md)                                                                                               | :heavy_minus_sign:                                                                                                                                     | The options for this request.                                                                                                                          |

### Response

**[*operations.DeleteToolRouteResponse](../../models/operations/deletetoolrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetToolDependentAgents

Get a list of agents depending on this tool

### Example Usage

<!-- UsageSnippet language="go" operationID="get_tool_dependent_agents_route" method="get" path="/v1/convai/tools/{tool_id}/dependent-agents" -->
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

    res, err := s.AgentsPlatform.GetToolDependentAgents(ctx, "<id>", nil, elevenlabsgo.Pointer[int64](30))
    if err != nil {
        log.Fatal(err)
    }
    if res.GetToolDependentAgentsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `ctx`                                                                        | [context.Context](https://pkg.go.dev/context#Context)                        | :heavy_check_mark:                                                           | The context to use for the request.                                          |
| `toolID`                                                                     | `string`                                                                     | :heavy_check_mark:                                                           | ID of the requested tool.                                                    |
| `cursor`                                                                     | `*string`                                                                    | :heavy_minus_sign:                                                           | Used for fetching next page. Cursor is returned in the response.             |
| `pageSize`                                                                   | `*int64`                                                                     | :heavy_minus_sign:                                                           | How many documents to return at maximum. Can not exceed 100, defaults to 30. |
| `opts`                                                                       | [][operations.Option](../../models/operations/option.md)                     | :heavy_minus_sign:                                                           | The options for this request.                                                |

### Response

**[*operations.GetToolDependentAgentsRouteResponse](../../models/operations/gettooldependentagentsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetToolExecutionsRoute

Get paginated list of tool executions for a specific tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_tool_executions_route" method="get" path="/v1/convai/tools/{tool_id}/executions" -->
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

    res, err := s.AgentsPlatform.GetToolExecutionsRoute(ctx, operations.GetToolExecutionsRouteRequest{
        ToolID: "<id>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetToolExecutionsPageResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                            | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                | :heavy_check_mark:                                                                                   | The context to use for the request.                                                                  |
| `request`                                                                                            | [operations.GetToolExecutionsRouteRequest](../../models/operations/gettoolexecutionsrouterequest.md) | :heavy_check_mark:                                                                                   | The request object to use for the request.                                                           |
| `opts`                                                                                               | [][operations.Option](../../models/operations/option.md)                                             | :heavy_minus_sign:                                                                                   | The options for this request.                                                                        |

### Response

**[*operations.GetToolExecutionsRouteResponse](../../models/operations/gettoolexecutionsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSettings

Retrieve Convai settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_settings_route" method="get" path="/v1/convai/settings" -->
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

    res, err := s.AgentsPlatform.GetSettings(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAISettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetSettingsRouteResponse](../../models/operations/getsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSettings

Update Convai settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="update_settings_route" method="patch" path="/v1/convai/settings" -->
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

    res, err := s.AgentsPlatform.UpdateSettings(ctx, components.PatchConvAISettingsRequest{
        ConversationInitiationClientDataWebhook: &components.ConversationInitiationClientDataWebhook{
            URL: "https://example.com/webhook",
            RequestHeaders: map[string]components.ConversationInitiationClientDataWebhookRequestHeaders{
                "Content-Type": components.CreateConversationInitiationClientDataWebhookRequestHeadersStr(
                    "application/json",
                ),
            },
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAISettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                      | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `ctx`                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                          | :heavy_check_mark:                                                                             | The context to use for the request.                                                            |
| `request`                                                                                      | [components.PatchConvAISettingsRequest](../../models/components/patchconvaisettingsrequest.md) | :heavy_check_mark:                                                                             | The request object to use for the request.                                                     |
| `opts`                                                                                         | [][operations.Option](../../models/operations/option.md)                                       | :heavy_minus_sign:                                                                             | The options for this request.                                                                  |

### Response

**[*operations.UpdateSettingsRouteResponse](../../models/operations/updatesettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetDashboardSettings

Retrieve Convai dashboard settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="get_dashboard_settings_route" method="get" path="/v1/convai/settings/dashboard" -->
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

    res, err := s.AgentsPlatform.GetDashboardSettings(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAIDashboardSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetDashboardSettingsRouteResponse](../../models/operations/getdashboardsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateDashboardSettings

Update Convai dashboard settings for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="update_dashboard_settings_route" method="patch" path="/v1/convai/settings/dashboard" -->
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

    res, err := s.AgentsPlatform.UpdateDashboardSettings(ctx, components.PatchConvAIDashboardSettingsRequest{})
    if err != nil {
        log.Fatal(err)
    }
    if res.GetConvAIDashboardSettingsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                        | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                            | :heavy_check_mark:                                                                                               | The context to use for the request.                                                                              |
| `request`                                                                                                        | [components.PatchConvAIDashboardSettingsRequest](../../models/components/patchconvaidashboardsettingsrequest.md) | :heavy_check_mark:                                                                                               | The request object to use for the request.                                                                       |
| `opts`                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                         | :heavy_minus_sign:                                                                                               | The options for this request.                                                                                    |

### Response

**[*operations.UpdateDashboardSettingsRouteResponse](../../models/operations/updatedashboardsettingsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateSecret

Create a new secret for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="create_secret_route" method="post" path="/v1/convai/secrets" -->
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

    res, err := s.AgentsPlatform.CreateSecret(ctx, components.PostWorkspaceSecretRequest{
        Name: "<value>",
        Value: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.PostWorkspaceSecretResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                      | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `ctx`                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                          | :heavy_check_mark:                                                                             | The context to use for the request.                                                            |
| `request`                                                                                      | [components.PostWorkspaceSecretRequest](../../models/components/postworkspacesecretrequest.md) | :heavy_check_mark:                                                                             | The request object to use for the request.                                                     |
| `opts`                                                                                         | [][operations.Option](../../models/operations/option.md)                                       | :heavy_minus_sign:                                                                             | The options for this request.                                                                  |

### Response

**[*operations.CreateSecretRouteResponse](../../models/operations/createsecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSecrets

Get all workspace secrets for the user

### Example Usage

<!-- UsageSnippet language="go" operationID="get_secrets_route" method="get" path="/v1/convai/secrets" -->
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

    res, err := s.AgentsPlatform.GetSecrets(ctx, nil, nil, nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetWorkspaceSecretsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                      | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                          | [context.Context](https://pkg.go.dev/context#Context)                                                          | :heavy_check_mark:                                                                                             | The context to use for the request.                                                                            |
| `pageSize`                                                                                                     | `*int64`                                                                                                       | :heavy_minus_sign:                                                                                             | How many documents to return at maximum. Can not exceed 100. If not provided, returns all secrets.             |
| `dependencyLimit`                                                                                              | `*int64`                                                                                                       | :heavy_minus_sign:                                                                                             | Maximum number of dependent resources (tools, agents, phone numbers) to return per secret. Can not exceed 100. |
| `search`                                                                                                       | `*string`                                                                                                      | :heavy_minus_sign:                                                                                             | If specified, returns only secrets whose names start with this string.                                         |
| `cursor`                                                                                                       | `*string`                                                                                                      | :heavy_minus_sign:                                                                                             | Used for fetching next page. Cursor is returned in the response.                                               |
| `opts`                                                                                                         | [][operations.Option](../../models/operations/option.md)                                                       | :heavy_minus_sign:                                                                                             | The options for this request.                                                                                  |

### Response

**[*operations.GetSecretsRouteResponse](../../models/operations/getsecretsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSecretRoute

Get a workspace secret by ID

### Example Usage

<!-- UsageSnippet language="go" operationID="get_secret_route" method="get" path="/v1/convai/secrets/{secret_id}" -->
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

    res, err := s.AgentsPlatform.GetSecretRoute(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.ConvAIWorkspaceStoredSecretConfig != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `secretID`                                               | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetSecretRouteResponse](../../models/operations/getsecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteSecret

Delete a workspace secret if it's not in use

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_secret_route" method="delete" path="/v1/convai/secrets/{secret_id}" -->
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

    res, err := s.AgentsPlatform.DeleteSecret(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `secretID`                                               | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.DeleteSecretRouteResponse](../../models/operations/deletesecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateSecret

Update an existing secret for the workspace

### Example Usage

<!-- UsageSnippet language="go" operationID="update_secret_route" method="patch" path="/v1/convai/secrets/{secret_id}" -->
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

    res, err := s.AgentsPlatform.UpdateSecret(ctx, "<id>", components.PatchWorkspaceSecretRequest{
        Name: "<value>",
        Value: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.PostWorkspaceSecretResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                        | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                            | :heavy_check_mark:                                                                               | The context to use for the request.                                                              |
| `secretID`                                                                                       | `string`                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `body`                                                                                           | [components.PatchWorkspaceSecretRequest](../../models/components/patchworkspacesecretrequest.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `opts`                                                                                           | [][operations.Option](../../models/operations/option.md)                                         | :heavy_minus_sign:                                                                               | The options for this request.                                                                    |

### Response

**[*operations.UpdateSecretRouteResponse](../../models/operations/updatesecretrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetSecretDependencies

Get paginated list of resources that depend on a specific secret, filtered by resource type.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_secret_dependencies_route" method="get" path="/v1/convai/secrets/{secret_id}/dependencies/{resource_type}" -->
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

    res, err := s.AgentsPlatform.GetSecretDependencies(ctx, "<id>", components.SecretDependencyResourceTypeAgents, elevenlabsgo.Pointer[int64](20), nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.GetSecretDependenciesResponseModel != nil {
        switch res.GetSecretDependenciesResponseModel.Dependencies.Type {
            case components.Dependencies3TypeArrayOfDependencies1:
                // res.GetSecretDependenciesResponseModel.Dependencies.ArrayOfDependencies1 is populated
            case components.Dependencies3TypeArrayOfDependencies2:
                // res.GetSecretDependenciesResponseModel.Dependencies.ArrayOfDependencies2 is populated
            case components.Dependencies3TypeArrayOfDependentPhoneNumberIdentifier:
                // res.GetSecretDependenciesResponseModel.Dependencies.ArrayOfDependentPhoneNumberIdentifier is populated
        }

    }
}
```

### Parameters

| Parameter                                                                                          | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                              | [context.Context](https://pkg.go.dev/context#Context)                                              | :heavy_check_mark:                                                                                 | The context to use for the request.                                                                |
| `secretID`                                                                                         | `string`                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `resourceType`                                                                                     | [components.SecretDependencyResourceType](../../models/components/secretdependencyresourcetype.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `pageSize`                                                                                         | `*int64`                                                                                           | :heavy_minus_sign:                                                                                 | How many dependency items to return per page.                                                      |
| `cursor`                                                                                           | `*string`                                                                                          | :heavy_minus_sign:                                                                                 | Used for fetching next page. Cursor is returned in the response.                                   |
| `opts`                                                                                             | [][operations.Option](../../models/operations/option.md)                                           | :heavy_minus_sign:                                                                                 | The options for this request.                                                                      |

### Response

**[*operations.GetSecretDependenciesRouteResponse](../../models/operations/getsecretdependenciesrouteresponse.md), error**

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.CreateBatchCall(ctx, components.BodySubmitABatchCallRequestV1ConvaiBatchCallingSubmitPost{
        CallName: "<value>",
        AgentID: "<id>",
        Recipients: []components.OutboundCallRecipient{},
    })
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
| `request`                                                                                                                                                    | [components.BodySubmitABatchCallRequestV1ConvaiBatchCallingSubmitPost](../../models/components/bodysubmitabatchcallrequestv1convaibatchcallingsubmitpost.md) | :heavy_check_mark:                                                                                                                                           | The request object to use for the request.                                                                                                                   |
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetWorkspaceBatchCalls(ctx, elevenlabsgo.Pointer[int64](100), nil, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.WorkspaceBatchCallsResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `limit`                                                  | `*int64`                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `lastDoc`                                                | `*string`                                                | :heavy_minus_sign:                                       | N/A                                                      |
| `agentID`                                                | `*string`                                                | :heavy_minus_sign:                                       | Filter batch calls to a single agent.                    |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetBatchCall(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallDetailedResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `batchID`                                                | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.DeleteBatchCall(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `batchID`                                                | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.CancelBatchCall(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `batchID`                                                | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.RetryBatchCall(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.BatchCallResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `batchID`                                                | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.HandleSipTrunkOutboundCall(ctx, components.BodyHandleAnOutboundCallViaSIPTrunkV1ConvaiSIPTrunkOutboundCallPost{
        AgentID: "<id>",
        AgentPhoneNumberID: "<id>",
        ToNumber: "<value>",
        ConversationInitiationClientData: &components.ConversationInitiationClientDataRequestInput{
            ConversationConfigOverride: &components.ConversationConfigClientOverrideInput{
                Asr: &components.ASRConversationalConfigOverride{
                    Keywords: []string{
                        "hello",
                        "world",
                    },
                },
                Turn: &components.TurnConfigOverride{
                    SoftTimeoutConfig: &components.SoftTimeoutConfigOverride{
                        Message: elevenlabsgo.Pointer("Hhmmmm...yeah."),
                    },
                },
                Tts: &components.TTSConversationalConfigOverride{
                    VoiceID: elevenlabsgo.Pointer("cjVigY5qzO86Huf0OWal"),
                    Stability: elevenlabsgo.Pointer[float64](0.5),
                    Speed: elevenlabsgo.Pointer[float64](1.0),
                    SimilarityBoost: elevenlabsgo.Pointer[float64](0.8),
                },
                Agent: &components.AgentConfigOverrideInput{
                    FirstMessage: elevenlabsgo.Pointer("Hello, how can I help you today?"),
                    Language: elevenlabsgo.Pointer("en"),
                    Prompt: &components.PromptAgentAPIModelOverrideInput{
                        Prompt: elevenlabsgo.Pointer("You are a helpful assistant that can answer questions about the topic of the conversation."),
                        Llm: components.LlmGemini20Flash001.ToPointer(),
                        ToolIds: []string{},
                        KnowledgeBase: []components.KnowledgeBaseLocator{},
                    },
                },
            },
        },
    })
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
| `request`                                                                                                                                                                        | [components.BodyHandleAnOutboundCallViaSIPTrunkV1ConvaiSIPTrunkOutboundCallPost](../../models/components/bodyhandleanoutboundcallviasiptrunkv1convaisiptrunkoutboundcallpost.md) | :heavy_check_mark:                                                                                                                                                               | The request object to use for the request.                                                                                                                                       |
| `opts`                                                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                                                         | :heavy_minus_sign:                                                                                                                                                               | The options for this request.                                                                                                                                                    |

### Response

**[*operations.HandleSipTrunkOutboundCallResponse](../../models/operations/handlesiptrunkoutboundcallresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateMcpServer

Create a new MCP server configuration in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="create_mcp_server_route" method="post" path="/v1/convai/mcp-servers" -->
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

    res, err := s.AgentsPlatform.CreateMcpServer(ctx, components.MCPServerRequestModel{
        Config: components.MCPServerConfigInput{
            URL: components.CreateMCPServerConfigInputURLStr(
                "https://babyish-injunction.info",
            ),
            Name: "<value>",
            ToolConfigOverrides: []components.MCPToolConfigOverrideInput{
                components.MCPToolConfigOverrideInput{
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
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |
| `request`                                                                            | [components.MCPServerRequestModel](../../models/components/mcpserverrequestmodel.md) | :heavy_check_mark:                                                                   | The request object to use for the request.                                           |
| `opts`                                                                               | [][operations.Option](../../models/operations/option.md)                             | :heavy_minus_sign:                                                                   | The options for this request.                                                        |

### Response

**[*operations.CreateMcpServerRouteResponse](../../models/operations/createmcpserverrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListMcpServers

Retrieve all MCP server configurations available in the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_mcp_servers_route" method="get" path="/v1/convai/mcp-servers" -->
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

    res, err := s.AgentsPlatform.ListMcpServers(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServersResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.ListMcpServersRouteResponse](../../models/operations/listmcpserversrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetMcp

Retrieve a specific MCP server configuration from the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_mcp_route" method="get" path="/v1/convai/mcp-servers/{mcp_server_id}" -->
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

    res, err := s.AgentsPlatform.GetMcp(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `mcpServerID`                                            | `string`                                                 | :heavy_check_mark:                                       | ID of the MCP Server.                                    |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetMcpRouteResponse](../../models/operations/getmcprouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteMcpServer

Delete a specific MCP server configuration from the workspace.

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_mcp_server_route" method="delete" path="/v1/convai/mcp-servers/{mcp_server_id}" -->
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

    res, err := s.AgentsPlatform.DeleteMcpServer(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `mcpServerID`                                            | `string`                                                 | :heavy_check_mark:                                       | ID of the MCP Server.                                    |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.DeleteMcpServerRouteResponse](../../models/operations/deletemcpserverrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateMcpServerConfig

Update the configuration settings for an MCP server.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_mcp_server_config_route" method="patch" path="/v1/convai/mcp-servers/{mcp_server_id}" -->
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

    res, err := s.AgentsPlatform.UpdateMcpServerConfig(ctx, "<id>", components.MCPServerConfigUpdateRequestModel{})
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                    | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                        | [context.Context](https://pkg.go.dev/context#Context)                                                        | :heavy_check_mark:                                                                                           | The context to use for the request.                                                                          |
| `mcpServerID`                                                                                                | `string`                                                                                                     | :heavy_check_mark:                                                                                           | ID of the MCP Server.                                                                                        |
| `body`                                                                                                       | [components.MCPServerConfigUpdateRequestModel](../../models/components/mcpserverconfigupdaterequestmodel.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `opts`                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                     | :heavy_minus_sign:                                                                                           | The options for this request.                                                                                |

### Response

**[*operations.UpdateMcpServerConfigRouteResponse](../../models/operations/updatemcpserverconfigrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ListMcpServerTools

Retrieve all tools available for a specific MCP server configuration.

### Example Usage

<!-- UsageSnippet language="go" operationID="list_mcp_server_tools_route" method="get" path="/v1/convai/mcp-servers/{mcp_server_id}/tools" -->
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

    res, err := s.AgentsPlatform.ListMcpServerTools(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.ListMCPToolsResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `mcpServerID`                                            | `string`                                                 | :heavy_check_mark:                                       | ID of the MCP Server.                                    |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.ListMcpServerToolsRouteResponse](../../models/operations/listmcpservertoolsrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## ~~UpdateMcpServerApprovalPolicy~~

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.UpdateMcpServerApprovalPolicy(ctx, "<id>", components.MCPApprovalPolicyUpdateRequestModel{})
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                        | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                            | :heavy_check_mark:                                                                                               | The context to use for the request.                                                                              |
| `mcpServerID`                                                                                                    | `string`                                                                                                         | :heavy_check_mark:                                                                                               | ID of the MCP Server.                                                                                            |
| `body`                                                                                                           | [components.MCPApprovalPolicyUpdateRequestModel](../../models/components/mcpapprovalpolicyupdaterequestmodel.md) | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `opts`                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                         | :heavy_minus_sign:                                                                                               | The options for this request.                                                                                    |

### Response

**[*operations.UpdateMcpServerApprovalPolicyRouteResponse](../../models/operations/updatemcpserverapprovalpolicyrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddMcpServerToolApproval

Add approval for a specific MCP tool when using per-tool approval mode.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_mcp_server_tool_approval_route" method="post" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-approvals" -->
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

    res, err := s.AgentsPlatform.AddMcpServerToolApproval(ctx, "<id>", components.MCPToolAddApprovalRequestModel{
        ToolName: "<value>",
        ToolDescription: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                              | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                  | [context.Context](https://pkg.go.dev/context#Context)                                                  | :heavy_check_mark:                                                                                     | The context to use for the request.                                                                    |
| `mcpServerID`                                                                                          | `string`                                                                                               | :heavy_check_mark:                                                                                     | ID of the MCP Server.                                                                                  |
| `body`                                                                                                 | [components.MCPToolAddApprovalRequestModel](../../models/components/mcptooladdapprovalrequestmodel.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `opts`                                                                                                 | [][operations.Option](../../models/operations/option.md)                                               | :heavy_minus_sign:                                                                                     | The options for this request.                                                                          |

### Response

**[*operations.AddMcpServerToolApprovalRouteResponse](../../models/operations/addmcpservertoolapprovalrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RemoveMcpServerToolApproval

Remove approval for a specific MCP tool when using per-tool approval mode.

### Example Usage

<!-- UsageSnippet language="go" operationID="remove_mcp_server_tool_approval_route" method="delete" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-approvals/{tool_name}" -->
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

    res, err := s.AgentsPlatform.RemoveMcpServerToolApproval(ctx, "<id>", "<value>")
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `mcpServerID`                                            | `string`                                                 | :heavy_check_mark:                                       | ID of the MCP Server.                                    |
| `toolName`                                               | `string`                                                 | :heavy_check_mark:                                       | Name of the MCP tool to remove approval for.             |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.RemoveMcpServerToolApprovalRouteResponse](../../models/operations/removemcpservertoolapprovalrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## AddMcpToolConfigOverride

Create configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="add_mcp_tool_config_override_route" method="post" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs" -->
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

    res, err := s.AgentsPlatform.AddMcpToolConfigOverride(ctx, "<id>", components.MCPToolConfigOverrideCreateRequestModel{
        Assignments: []components.DynamicVariableAssignment{
            components.DynamicVariableAssignment{
                DynamicVariable: "user_name",
                ValuePath: "user.name",
            },
        },
        ToolName: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `mcpServerID`                                                                                                            | `string`                                                                                                                 | :heavy_check_mark:                                                                                                       | ID of the MCP Server.                                                                                                    |
| `body`                                                                                                                   | [components.MCPToolConfigOverrideCreateRequestModel](../../models/components/mcptoolconfigoverridecreaterequestmodel.md) | :heavy_check_mark:                                                                                                       | N/A                                                                                                                      |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.AddMcpToolConfigOverrideRouteResponse](../../models/operations/addmcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetMcpToolConfigOverride

Retrieve configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="get_mcp_tool_config_override_route" method="get" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs/{tool_name}" -->
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

    res, err := s.AgentsPlatform.GetMcpToolConfigOverride(ctx, "<id>", "<value>")
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPToolConfigOverrideOutput != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `mcpServerID`                                            | `string`                                                 | :heavy_check_mark:                                       | ID of the MCP Server.                                    |
| `toolName`                                               | `string`                                                 | :heavy_check_mark:                                       | Name of the MCP tool to retrieve config overrides for.   |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.GetMcpToolConfigOverrideRouteResponse](../../models/operations/getmcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateMcpToolConfigOverride

Update configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="update_mcp_tool_config_override_route" method="patch" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs/{tool_name}" -->
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

    res, err := s.AgentsPlatform.UpdateMcpToolConfigOverride(ctx, "<id>", "<value>", components.MCPToolConfigOverrideUpdateRequestModel{
        Assignments: []components.DynamicVariableAssignment{
            components.DynamicVariableAssignment{
                DynamicVariable: "user_name",
                ValuePath: "user.name",
            },
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                | Type                                                                                                                     | Required                                                                                                                 | Description                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                                                    | :heavy_check_mark:                                                                                                       | The context to use for the request.                                                                                      |
| `mcpServerID`                                                                                                            | `string`                                                                                                                 | :heavy_check_mark:                                                                                                       | ID of the MCP Server.                                                                                                    |
| `toolName`                                                                                                               | `string`                                                                                                                 | :heavy_check_mark:                                                                                                       | Name of the MCP tool to update config overrides for.                                                                     |
| `body`                                                                                                                   | [components.MCPToolConfigOverrideUpdateRequestModel](../../models/components/mcptoolconfigoverrideupdaterequestmodel.md) | :heavy_check_mark:                                                                                                       | N/A                                                                                                                      |
| `opts`                                                                                                                   | [][operations.Option](../../models/operations/option.md)                                                                 | :heavy_minus_sign:                                                                                                       | The options for this request.                                                                                            |

### Response

**[*operations.UpdateMcpToolConfigOverrideRouteResponse](../../models/operations/updatemcptoolconfigoverriderouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RemoveMcpToolConfigOverride

Remove configuration overrides for a specific MCP tool.

### Example Usage

<!-- UsageSnippet language="go" operationID="remove_mcp_tool_config_override_route" method="delete" path="/v1/convai/mcp-servers/{mcp_server_id}/tool-configs/{tool_name}" -->
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

    res, err := s.AgentsPlatform.RemoveMcpToolConfigOverride(ctx, "<id>", "<value>")
    if err != nil {
        log.Fatal(err)
    }
    if res.MCPServerResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `mcpServerID`                                            | `string`                                                 | :heavy_check_mark:                                       | ID of the MCP Server.                                    |
| `toolName`                                               | `string`                                                 | :heavy_check_mark:                                       | Name of the MCP tool to remove config overrides for.     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.RemoveMcpToolConfigOverrideRouteResponse](../../models/operations/removemcptoolconfigoverriderouteresponse.md), error**

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetWhatsappAccount(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.GetWhatsAppAccountResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `phoneNumberID`                                          | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.DeleteWhatsappAccount(ctx, "<id>")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `phoneNumberID`                                          | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.UpdateWhatsappAccount(ctx, "<id>", components.UpdateWhatsAppAccountRequest{})
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
| `phoneNumberID`                                                                                    | `string`                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `body`                                                                                             | [components.UpdateWhatsAppAccountRequest](../../models/components/updatewhatsappaccountrequest.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `opts`                                                                                             | [][operations.Option](../../models/operations/option.md)                                           | :heavy_minus_sign:                                                                                 | The options for this request.                                                                      |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.ListWhatsappAccounts(ctx, nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.ListWhatsAppAccountsResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `agentID`                                                | `*string`                                                | :heavy_minus_sign:                                       | Filter by assigned agent ID                              |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

### Response

**[*operations.ListWhatsappAccountsResponse](../../models/operations/listwhatsappaccountsresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateBranch

Create a new branch from a given version of any branch

### Example Usage

<!-- UsageSnippet language="go" operationID="create_branch_route" method="post" path="/v1/convai/agents/{agent_id}/branches" -->
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

    res, err := s.AgentsPlatform.CreateBranch(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodyCreateANewBranchV1ConvaiAgentsAgentIDBranchesPost{
        ParentVersionID: "<id>",
        Name: "<value>",
        Description: "faithfully platter equally red",
        Workflow: &components.AgentWorkflowRequestModel{
            Edges: map[string]components.WorkflowEdgeModelInput{
                "entry_to_tool_a": components.WorkflowEdgeModelInput{
                    Source: "entry_node",
                    Target: "tool_node_a",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: true,
                        },
                    )),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputAddOperator(
                                components.ASTAdditionOperatorNodeInput1{
                                    Left: components.CreateASTNodeInputLlm(
                                        components.CreateASTLLMNodeInputASTLLMNode1(
                                            components.ASTLLMNode1{
                                                ValueSchema: components.LLMLiteralJSONSchemaProperty{
                                                    Type: components.CreateLLMLiteralJSONSchemaPropertyTypeUnionLLMLiteralJSONSchemaPropertyTypeEnum(
                                                        components.LLMLiteralJSONSchemaPropertyTypeEnumNumber,
                                                    ),
                                                    Description: "ashamed golden wide-eyed deduce kiddingly sure-footed",
                                                },
                                            },
                                        ),
                                    ),
                                    Right: components.CreateASTNodeInputDynamicVariable(
                                        components.ASTDynamicVariableNodeInput{
                                            Name: "<value>",
                                        },
                                    ),
                                },
                            ),
                        },
                    )),
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputAndOperator(
                                components.ASTAndOperatorNodeInput1{
                                    Children: []components.ASTNodeInput{},
                                },
                            ),
                        },
                    )),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputLlm(
                                components.CreateASTLLMNodeInputASTLLMNode2(
                                    components.ASTLLMNode2{
                                        Prompt: "<value>",
                                    },
                                ),
                            ),
                        },
                    )),
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
                        AgentID: elevenlabsgo.Pointer("<id>"),
                    },
                ),
                "tool_node_a": components.CreateAgentWorkflowRequestModelNodesStart(
                    components.WorkflowStartNodeModelInput{},
                ),
                "tool_node_b": components.CreateAgentWorkflowRequestModelNodesTool(
                    components.WorkflowToolNodeModelInput{},
                ),
            },
        },
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.CreateAgentBranchResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                            | Type                                                                                                                                                 | Required                                                                                                                                             | Description                                                                                                                                          | Example                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                                                                                | :heavy_check_mark:                                                                                                                                   | The context to use for the request.                                                                                                                  |                                                                                                                                                      |
| `agentID`                                                                                                                                            | `string`                                                                                                                                             | :heavy_check_mark:                                                                                                                                   | The id of an agent. This is returned on agent creation.                                                                                              | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                   |
| `body`                                                                                                                                               | [components.BodyCreateANewBranchV1ConvaiAgentsAgentIDBranchesPost](../../models/components/bodycreateanewbranchv1convaiagentsagentidbranchespost.md) | :heavy_check_mark:                                                                                                                                   | N/A                                                                                                                                                  |                                                                                                                                                      |
| `opts`                                                                                                                                               | [][operations.Option](../../models/operations/option.md)                                                                                             | :heavy_minus_sign:                                                                                                                                   | The options for this request.                                                                                                                        |                                                                                                                                                      |

### Response

**[*operations.CreateBranchRouteResponse](../../models/operations/createbranchrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetBranches

Returns a list of branches an agent has

### Example Usage

<!-- UsageSnippet language="go" operationID="get_branches_route" method="get" path="/v1/convai/agents/{agent_id}/branches" -->
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

    res, err := s.AgentsPlatform.GetBranches(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", elevenlabsgo.Pointer(false), elevenlabsgo.Pointer[int64](100))
    if err != nil {
        log.Fatal(err)
    }
    if res.ListResponseAgentBranchSummary != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `includeArchived`                                        | `*bool`                                                  | :heavy_minus_sign:                                       | Whether archived branches should be included             |                                                          |
| `limit`                                                  | `*int64`                                                 | :heavy_minus_sign:                                       | How many results at most should be returned              |                                                          |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetBranchesRouteResponse](../../models/operations/getbranchesrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetBranch

Get information about a single agent branch

### Example Usage

<!-- UsageSnippet language="go" operationID="get_branch_route" method="get" path="/v1/convai/agents/{agent_id}/branches/{branch_id}" -->
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

    res, err := s.AgentsPlatform.GetBranch(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbranch_0901k4aafjxxfxt93gd841r7tv5t")
    if err != nil {
        log.Fatal(err)
    }
    if res.AgentBranchResponse != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `branchID`                                               | `string`                                                 | :heavy_check_mark:                                       | Unique identifier for the branch.                        | agtbranch_0901k4aafjxxfxt93gd841r7tv5t                   |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetBranchRouteResponse](../../models/operations/getbranchrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## UpdateBranch

Update agent branch properties such as archiving status and protection level

### Example Usage

<!-- UsageSnippet language="go" operationID="update_branch_route" method="patch" path="/v1/convai/agents/{agent_id}/branches/{branch_id}" -->
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

    res, err := s.AgentsPlatform.UpdateBranch(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbranch_0901k4aafjxxfxt93gd841r7tv5t", nil)
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
| `body`                                                                                                                                                                    | [*components.BodyUpdateAgentBranchV1ConvaiAgentsAgentIDBranchesBranchIDPatch](../../models/components/bodyupdateagentbranchv1convaiagentsagentidbranchesbranchidpatch.md) | :heavy_minus_sign:                                                                                                                                                        | N/A                                                                                                                                                                       |                                                                                                                                                                           |
| `opts`                                                                                                                                                                    | [][operations.Option](../../models/operations/option.md)                                                                                                                  | :heavy_minus_sign:                                                                                                                                                        | The options for this request.                                                                                                                                             |                                                                                                                                                                           |

### Response

**[*operations.UpdateBranchRouteResponse](../../models/operations/updatebranchrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## GetVersionMetadataRoute

Get metadata for a specific agent version

### Example Usage

<!-- UsageSnippet language="go" operationID="get_version_metadata_route" method="get" path="/v1/convai/agents/{agent_id}/versions/{version_id}" -->
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

    res, err := s.AgentsPlatform.GetVersionMetadataRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtvrsn_0901k4aafjxxfxt93gd841r7tv5t")
    if err != nil {
        log.Fatal(err)
    }
    if res.AgentVersionMetadata != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `versionID`                                              | `string`                                                 | :heavy_check_mark:                                       | Unique identifier for the version.                       | agtvrsn_0901k4aafjxxfxt93gd841r7tv5t                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.GetVersionMetadataRouteResponse](../../models/operations/getversionmetadatarouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## MergePreviewRoute

Returns the result of merging the source branch into the target branch without performing the merge. Useful for showing an accurate diff before confirming.

### Example Usage

<!-- UsageSnippet language="go" operationID="merge_preview_route" method="get" path="/v1/convai/agents/{agent_id}/branches/{source_branch_id}/merge-preview" -->
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

    res, err := s.AgentsPlatform.MergePreviewRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", elevenlabsgo.Pointer(false))
    if err != nil {
        log.Fatal(err)
    }
    if res.MergePreviewResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `ctx`                                                                          | [context.Context](https://pkg.go.dev/context#Context)                          | :heavy_check_mark:                                                             | The context to use for the request.                                            |                                                                                |
| `agentID`                                                                      | `string`                                                                       | :heavy_check_mark:                                                             | The id of an agent. This is returned on agent creation.                        | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                             |
| `sourceBranchID`                                                               | `string`                                                                       | :heavy_check_mark:                                                             | Unique identifier for the source branch to merge from.                         | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                           |
| `targetBranchID`                                                               | `string`                                                                       | :heavy_check_mark:                                                             | The ID of the target branch to merge into.                                     | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                           |
| `force`                                                                        | `*bool`                                                                        | :heavy_minus_sign:                                                             | When true, source branch changes always win conflicts regardless of timestamps |                                                                                |
| `opts`                                                                         | [][operations.Option](../../models/operations/option.md)                       | :heavy_minus_sign:                                                             | The options for this request.                                                  |                                                                                |

### Response

**[*operations.MergePreviewRouteResponse](../../models/operations/mergepreviewrouteresponse.md), error**

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.MergeBranchIntoTarget(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", nil)
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                                                                                                                                             | Type                                                                                                                                                                                                                  | Required                                                                                                                                                                                                              | Description                                                                                                                                                                                                           | Example                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                                                                                                                                 | [context.Context](https://pkg.go.dev/context#Context)                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                                                    | The context to use for the request.                                                                                                                                                                                   |                                                                                                                                                                                                                       |
| `agentID`                                                                                                                                                                                                             | `string`                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                    | The id of an agent. This is returned on agent creation.                                                                                                                                                               | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                                                                                                    |
| `sourceBranchID`                                                                                                                                                                                                      | `string`                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                    | Unique identifier for the source branch to merge from.                                                                                                                                                                | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                                                                                                                                                                  |
| `targetBranchID`                                                                                                                                                                                                      | `string`                                                                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                                    | The ID of the target branch to merge into.                                                                                                                                                                            | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                                                                                                                                                                  |
| `body`                                                                                                                                                                                                                | [*components.BodyMergeABranchIntoATargetBranchV1ConvaiAgentsAgentIDBranchesSourceBranchIDMergePost](../../models/components/bodymergeabranchintoatargetbranchv1convaiagentsagentidbranchessourcebranchidmergepost.md) | :heavy_minus_sign:                                                                                                                                                                                                    | N/A                                                                                                                                                                                                                   |                                                                                                                                                                                                                       |
| `opts`                                                                                                                                                                                                                | [][operations.Option](../../models/operations/option.md)                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                                                    | The options for this request.                                                                                                                                                                                         |                                                                                                                                                                                                                       |

### Response

**[*operations.MergeBranchIntoTargetResponse](../../models/operations/mergebranchintotargetresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RebasePreviewRoute

Returns the result of rebasing the branch onto main without performing the rebase. Useful for showing an accurate diff before confirming.

### Example Usage

<!-- UsageSnippet language="go" operationID="rebase_preview_route" method="get" path="/v1/convai/agents/{agent_id}/branches/{branch_id}/rebase-preview" -->
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

    res, err := s.AgentsPlatform.RebasePreviewRoute(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj")
    if err != nil {
        log.Fatal(err)
    }
    if res.MergePreviewResponseModel != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `branchID`                                               | `string`                                                 | :heavy_check_mark:                                       | Unique identifier for the source branch to merge from.   | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.RebasePreviewRouteResponse](../../models/operations/rebasepreviewrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## RebaseBranchOntoMain

Rebase a branch onto the latest main branch, incorporating main's changes while preserving the branch's own changes.

### Example Usage

<!-- UsageSnippet language="go" operationID="rebase_branch_onto_main" method="post" path="/v1/convai/agents/{agent_id}/branches/{branch_id}/rebase" -->
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

    res, err := s.AgentsPlatform.RebaseBranchOntoMain(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `branchID`                                               | `string`                                                 | :heavy_check_mark:                                       | Unique identifier for the source branch to merge from.   | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

### Response

**[*operations.RebaseBranchOntoMainResponse](../../models/operations/rebasebranchontomainresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentDeployment

Create a new deployment for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_deployment_route" method="post" path="/v1/convai/agents/{agent_id}/deployments" -->
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

    res, err := s.AgentsPlatform.CreateAgentDeployment(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", components.BodyCreateOrUpdateDeploymentsV1ConvaiAgentsAgentIDDeploymentsPost{
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
    })
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
| `opts`                                                                                                                                                                       | [][operations.Option](../../models/operations/option.md)                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | The options for this request.                                                                                                                                                |                                                                                                                                                                              |

### Response

**[*operations.CreateAgentDeploymentRouteResponse](../../models/operations/createagentdeploymentrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## CreateAgentDraft

Create a new draft for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="create_agent_draft_route" method="post" path="/v1/convai/agents/{agent_id}/drafts" -->
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

    res, err := s.AgentsPlatform.CreateAgentDraft(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj", components.BodyCreateAgentDraftV1ConvaiAgentsAgentIDDraftsPost{
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
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "start_to_entry": components.WorkflowEdgeModelInput{
                    Source: "start_node",
                    Target: "entry_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_a_to_failure": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "failure_node",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionExpression(
                        components.WorkflowExpressionConditionModelInput{
                            Expression: components.CreateASTNodeInputStringLiteral(
                                components.ASTStringNodeInput{
                                    Value: "<value>",
                                },
                            ),
                        },
                    )),
                },
                "tool_a_to_tool_b": components.WorkflowEdgeModelInput{
                    Source: "tool_node_a",
                    Target: "tool_node_b",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_agent_transfer": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_transfer",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_conversation": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_conversation",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionLlm(
                        components.WorkflowLLMConditionModelInput{
                            Condition: "User's last message contains a question about our pricing.",
                        },
                    )),
                },
                "tool_b_to_end": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_end",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionUnconditional(
                        components.WorkflowUnconditionalModelInput{},
                    )),
                },
                "tool_b_to_phone": components.WorkflowEdgeModelInput{
                    Source: "tool_node_b",
                    Target: "success_phone",
                    ForwardCondition: elevenlabsgo.Pointer(components.CreateWorkflowEdgeModelInputForwardConditionResult(
                        components.WorkflowResultConditionModelInput{
                            Successful: false,
                        },
                    )),
                },
            },
            Nodes: map[string]components.AgentWorkflowRequestModelNodes{
                "entry_node": components.CreateAgentWorkflowRequestModelNodesEnd(
                    components.WorkflowEndNodeModelInput{},
                ),
                "failure_node": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: elevenlabsgo.Pointer("<id>"),
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
                        AgentID: elevenlabsgo.Pointer("<id>"),
                    },
                ),
                "success_transfer": components.CreateAgentWorkflowRequestModelNodesStandaloneAgent(
                    components.WorkflowStandaloneAgentNodeModelInput{
                        AgentID: elevenlabsgo.Pointer("<id>"),
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
        Tags: []string{
            "Customer Support",
            "Technical Help",
            "Eleven",
        },
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

| Parameter                                                                                                                                        | Type                                                                                                                                             | Required                                                                                                                                         | Description                                                                                                                                      | Example                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `ctx`                                                                                                                                            | [context.Context](https://pkg.go.dev/context#Context)                                                                                            | :heavy_check_mark:                                                                                                                               | The context to use for the request.                                                                                                              |                                                                                                                                                  |
| `agentID`                                                                                                                                        | `string`                                                                                                                                         | :heavy_check_mark:                                                                                                                               | The id of an agent. This is returned on agent creation.                                                                                          | agent_3701k3ttaq12ewp8b7qv5rfyszkz                                                                                                               |
| `branchID`                                                                                                                                       | `string`                                                                                                                                         | :heavy_check_mark:                                                                                                                               | The ID of the agent branch to use                                                                                                                | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                                                                                                             |
| `body`                                                                                                                                           | [components.BodyCreateAgentDraftV1ConvaiAgentsAgentIDDraftsPost](../../models/components/bodycreateagentdraftv1convaiagentsagentiddraftspost.md) | :heavy_check_mark:                                                                                                                               | N/A                                                                                                                                              |                                                                                                                                                  |
| `opts`                                                                                                                                           | [][operations.Option](../../models/operations/option.md)                                                                                         | :heavy_minus_sign:                                                                                                                               | The options for this request.                                                                                                                    |                                                                                                                                                  |

### Response

**[*operations.CreateAgentDraftRouteResponse](../../models/operations/createagentdraftrouteresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |

## DeleteAgentDraft

Delete a draft for an agent

### Example Usage

<!-- UsageSnippet language="go" operationID="delete_agent_draft_route" method="delete" path="/v1/convai/agents/{agent_id}/drafts" -->
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

    res, err := s.AgentsPlatform.DeleteAgentDraft(ctx, "agent_3701k3ttaq12ewp8b7qv5rfyszkz", "agtbrch_8901k4t9z5defmb8vh3e9361y7nj")
    if err != nil {
        log.Fatal(err)
    }
    if res.Any != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |                                                          |
| `agentID`                                                | `string`                                                 | :heavy_check_mark:                                       | The id of an agent. This is returned on agent creation.  | agent_3701k3ttaq12ewp8b7qv5rfyszkz                       |
| `branchID`                                               | `string`                                                 | :heavy_check_mark:                                       | The ID of the agent branch to use                        | agtbrch_8901k4t9z5defmb8vh3e9361y7nj                     |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |                                                          |

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
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.CreateEnvironmentVariable(ctx, operations.CreateCreateEnvironmentVariableRequestAuthConnection(
        components.CreateAuthConnectionEnvironmentVariableRequest{
            Label: "<value>",
            Values: map[string]components.EnvironmentVariableAuthConnectionValueRequest{

            },
        },
    ))
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
        }

    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `request`                                                                                                  | [operations.CreateEnvironmentVariableRequest](../../models/operations/createenvironmentvariablerequest.md) | :heavy_check_mark:                                                                                         | The request object to use for the request.                                                                 |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

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
	"log"
	"github.com/bdlilley/elevenlabs-go/models/components"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.GetEnvironmentVariable(ctx, "<id>")
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
        }

    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `envVarID`                                               | `string`                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `opts`                                                   | [][operations.Option](../../models/operations/option.md) | :heavy_minus_sign:                                       | The options for this request.                            |

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
	"log"
)

func main() {
    ctx := context.Background()

    s := elevenlabsgo.New(
        elevenlabsgo.WithSecurity("YOUR_API_KEY"),
    )

    res, err := s.AgentsPlatform.UpdateEnvironmentVariable(ctx, "<id>", components.UpdateEnvironmentVariableRequest{
        Values: map[string]*components.UpdateEnvironmentVariableRequestValues{

        },
    })
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
        }

    }
}
```

### Parameters

| Parameter                                                                                                  | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `ctx`                                                                                                      | [context.Context](https://pkg.go.dev/context#Context)                                                      | :heavy_check_mark:                                                                                         | The context to use for the request.                                                                        |
| `envVarID`                                                                                                 | `string`                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `body`                                                                                                     | [components.UpdateEnvironmentVariableRequest](../../models/components/updateenvironmentvariablerequest.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `opts`                                                                                                     | [][operations.Option](../../models/operations/option.md)                                                   | :heavy_minus_sign:                                                                                         | The options for this request.                                                                              |

### Response

**[*operations.UpdateEnvironmentVariableResponse](../../models/operations/updateenvironmentvariableresponse.md), error**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| apierrors.HTTPValidationError | 422                           | application/json              |
| apierrors.APIError            | 4XX, 5XX                      | \*/\*                         |