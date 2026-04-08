# elevenlabs-go 

Developer-friendly & type-safe Go SDK specifically catered to leverage *Elevenlabs* API.

[![Built by Speakeasy](https://img.shields.io/badge/Built_by-SPEAKEASY-374151?style=for-the-badge&labelColor=f3f4f6)](https://www.speakeasy.com/?utm_source=elevenlabs-go&utm_campaign=go)
[![License: MIT](https://img.shields.io/badge/LICENSE_//_MIT-3b5bdb?style=for-the-badge&labelColor=eff6ff)](https://opensource.org/licenses/MIT)


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/kudos/elevenlabs-go). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

ElevenLabs API Documentation: This is the documentation for the ElevenLabs API. You can use this API to use our service programmatically, this is done by using your API key. You can find your API key in the dashboard at https://elevenlabs.io/app/settings/api-keys.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [elevenlabs-go](#elevenlabs-go)
  * [SDK Installation](#sdk-installation)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Custom HTTP Client](#custom-http-client)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

To add the SDK as a dependency to your project:
```bash
go get github.com/bdlilley/elevenlabs-go
```
<!-- End SDK Installation [installation] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```go
package main

import (
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

	res, err := s.GetUserSubscriptionInfo(ctx, optionalnullable.From[string](nil))
	if err != nil {
		log.Fatal(err)
	}
	if res.ExtendedSubscriptionResponseModel != nil {
		switch res.ExtendedSubscriptionResponseModel.PendingChange.Type {
		case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingSubscriptionSwitchResponseModel is populated
		case components.PendingChangeTypePendingCancellationResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingCancellationResponseModel is populated
		}

	}
}

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name     | Type   | Scheme  |
| -------- | ------ | ------- |
| `APIKey` | apiKey | API key |

You can configure it using the `WithSecurity` option when initializing the SDK client instance. For example:
```go
package main

import (
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

	res, err := s.GetUserSubscriptionInfo(ctx, optionalnullable.From[string](nil))
	if err != nil {
		log.Fatal(err)
	}
	if res.ExtendedSubscriptionResponseModel != nil {
		switch res.ExtendedSubscriptionResponseModel.PendingChange.Type {
		case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingSubscriptionSwitchResponseModel is populated
		case components.PendingChangeTypePendingCancellationResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingCancellationResponseModel is populated
		}

	}
}

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [ElevenlabsGo SDK](docs/sdks/elevenlabsgo/README.md)

* [GetUserSubscriptionInfo](docs/sdks/elevenlabsgo/README.md#getusersubscriptioninfo) - Get User Subscription Info
* [GetUserInfo](docs/sdks/elevenlabsgo/README.md#getuserinfo) - Get User Info
* [UsageCharacters](docs/sdks/elevenlabsgo/README.md#usagecharacters) - Get Characters Usage Metrics
* [CreateAgentResponseTestRoute](docs/sdks/elevenlabsgo/README.md#createagentresponsetestroute) - Create Agent Response Test
* [GetAgentResponseTestRoute](docs/sdks/elevenlabsgo/README.md#getagentresponsetestroute) - Get Agent Response Test By Id
* [UpdateAgentResponseTestRoute](docs/sdks/elevenlabsgo/README.md#updateagentresponsetestroute) - Update Agent Response Test
* [DeleteChatResponseTestRoute](docs/sdks/elevenlabsgo/README.md#deletechatresponsetestroute) - Delete Agent Response Test
* [GetAgentResponseTestsSummariesRoute](docs/sdks/elevenlabsgo/README.md#getagentresponsetestssummariesroute) - Get Agent Response Test Summaries By Ids
* [ListChatResponseTestsRoute](docs/sdks/elevenlabsgo/README.md#listchatresponsetestsroute) - List Agent Response Tests
* [ListTestInvocationsRoute](docs/sdks/elevenlabsgo/README.md#listtestinvocationsroute) - List Test Invocations
* [RunAgentTestSuiteRoute](docs/sdks/elevenlabsgo/README.md#runagenttestsuiteroute) - Run Tests On The Agent
* [GetTestInvocationRoute](docs/sdks/elevenlabsgo/README.md#gettestinvocationroute) - Get Test Invocation
* [ResubmitTestsRoute](docs/sdks/elevenlabsgo/README.md#resubmittestsroute) - Resubmit Tests
* [RedirectToMintlify](docs/sdks/elevenlabsgo/README.md#redirecttomintlify) - Redirect To Mintlify

### [AgentsPlatform](docs/sdks/agentsplatform/README.md)

* [GetConversationSignedLink](docs/sdks/agentsplatform/README.md#getconversationsignedlink) - Get Signed Url
* [~~GetSignedURLDeprecated~~](docs/sdks/agentsplatform/README.md#getsignedurldeprecated) - Get Signed Url :warning: **Deprecated**
* [GetLivekitToken](docs/sdks/agentsplatform/README.md#getlivekittoken) - Get Webrtc Token
* [HandleTwilioOutboundCall](docs/sdks/agentsplatform/README.md#handletwiliooutboundcall) - Handle An Outbound Call Via Twilio
* [RegisterTwilioCall](docs/sdks/agentsplatform/README.md#registertwiliocall) - Register A Twilio Call And Return Twiml
* [WhatsappOutboundCall](docs/sdks/agentsplatform/README.md#whatsappoutboundcall) - Make An Outbound Call Via Whatsapp
* [WhatsappOutboundMessage](docs/sdks/agentsplatform/README.md#whatsappoutboundmessage) - Send An Outbound Message Via Whatsapp
* [CreateAgentRoute](docs/sdks/agentsplatform/README.md#createagentroute) - Create Agent
* [GetAgentSummariesRoute](docs/sdks/agentsplatform/README.md#getagentsummariesroute) - Get Agent Summaries
* [GetAgentRoute](docs/sdks/agentsplatform/README.md#getagentroute) - Get Agent
* [DeleteAgentRoute](docs/sdks/agentsplatform/README.md#deleteagentroute) - Delete Agent
* [PatchAgentSettingsRoute](docs/sdks/agentsplatform/README.md#patchagentsettingsroute) - Patches An Agent Settings
* [GetAgentWidgetRoute](docs/sdks/agentsplatform/README.md#getagentwidgetroute) - Get Agent Widget Config
* [GetAgentLinkRoute](docs/sdks/agentsplatform/README.md#getagentlinkroute) - Get Shareable Agent Link
* [PostAgentAvatarRoute](docs/sdks/agentsplatform/README.md#postagentavatarroute) - Post Agent Avatar
* [GetAgentsRoute](docs/sdks/agentsplatform/README.md#getagentsroute) - List Agents
* [GetAgentKnowledgeBaseSize](docs/sdks/agentsplatform/README.md#getagentknowledgebasesize) - Returns The Size Of The Agent'S Knowledge Base
* [GetAgentLlmExpectedCostCalculation](docs/sdks/agentsplatform/README.md#getagentllmexpectedcostcalculation) - Calculate Expected Llm Usage For An Agent
* [DuplicateAgentRoute](docs/sdks/agentsplatform/README.md#duplicateagentroute) - Duplicate Agent
* [RunConversationSimulationRoute](docs/sdks/agentsplatform/README.md#runconversationsimulationroute) - Simulates A Conversation
* [RunConversationSimulationRouteStream](docs/sdks/agentsplatform/README.md#runconversationsimulationroutestream) - Simulates A Conversation (Stream)
* [CreateAgentTestFolderRoute](docs/sdks/agentsplatform/README.md#createagenttestfolderroute) - Create Agent Test Folder
* [GetAgentTestFolderRoute](docs/sdks/agentsplatform/README.md#getagenttestfolderroute) - Get Agent Test Folder By Id
* [DeleteAgentTestFolderRoute](docs/sdks/agentsplatform/README.md#deleteagenttestfolderroute) - Delete Agent Test Folder
* [UpdateAgentTestFolderRoute](docs/sdks/agentsplatform/README.md#updateagenttestfolderroute) - Update Agent Test Folder
* [AgentTestingBulkMoveRoute](docs/sdks/agentsplatform/README.md#agenttestingbulkmoveroute) - Bulk Move Tests To Folder
* [GetConversationHistoriesRoute](docs/sdks/agentsplatform/README.md#getconversationhistoriesroute) - Get Conversations
* [GetConversationUsersRoute](docs/sdks/agentsplatform/README.md#getconversationusersroute) - Get Conversation Users
* [GetConversationHistoryRoute](docs/sdks/agentsplatform/README.md#getconversationhistoryroute) - Get Conversation Details
* [DeleteConversationRoute](docs/sdks/agentsplatform/README.md#deleteconversationroute) - Delete Conversation
* [GetConversationAudioRoute](docs/sdks/agentsplatform/README.md#getconversationaudioroute) - Get Conversation Audio
* [PostConversationFeedbackRoute](docs/sdks/agentsplatform/README.md#postconversationfeedbackroute) - Send Conversation Feedback
* [TextSearchConversationMessagesRoute](docs/sdks/agentsplatform/README.md#textsearchconversationmessagesroute) - Text Search Conversation Messages
* [SmartSearchConversationMessagesRoute](docs/sdks/agentsplatform/README.md#smartsearchconversationmessagesroute) - Smart Search Conversation Messages
* [ListPhoneNumbersRoute](docs/sdks/agentsplatform/README.md#listphonenumbersroute) - List Phone Numbers
* [CreatePhoneNumberRoute](docs/sdks/agentsplatform/README.md#createphonenumberroute) - Import Phone Number
* [GetPhoneNumberRoute](docs/sdks/agentsplatform/README.md#getphonenumberroute) - Get Phone Number
* [DeletePhoneNumberRoute](docs/sdks/agentsplatform/README.md#deletephonenumberroute) - Delete Phone Number
* [UpdatePhoneNumberRoute](docs/sdks/agentsplatform/README.md#updatephonenumberroute) - Update Phone Number
* [GetPublicLlmExpectedCostCalculation](docs/sdks/agentsplatform/README.md#getpublicllmexpectedcostcalculation) - Calculate Expected Llm Usage
* [ListAvailableLlms](docs/sdks/agentsplatform/README.md#listavailablellms) - List Available Llms
* [UploadFileRoute](docs/sdks/agentsplatform/README.md#uploadfileroute) - Upload File
* [CancelFileUploadRoute](docs/sdks/agentsplatform/README.md#cancelfileuploadroute) - Delete File Upload
* [GetLiveCount](docs/sdks/agentsplatform/README.md#getlivecount) - Get Live Count
* [GetAgentKnowledgeBaseSummariesRoute](docs/sdks/agentsplatform/README.md#getagentknowledgebasesummariesroute) - Get Knowledge Base Summaries By Ids
* [GetKnowledgeBaseListRoute](docs/sdks/agentsplatform/README.md#getknowledgebaselistroute) - Get Knowledge Base List
* [~~AddDocumentationToKnowledgeBase~~](docs/sdks/agentsplatform/README.md#adddocumentationtoknowledgebase) - Add To Knowledge Base :warning: **Deprecated**
* [CreateURLDocumentRoute](docs/sdks/agentsplatform/README.md#createurldocumentroute) - Create Url Document
* [CreateFileDocumentRoute](docs/sdks/agentsplatform/README.md#createfiledocumentroute) - Create File Document
* [CreateTextDocumentRoute](docs/sdks/agentsplatform/README.md#createtextdocumentroute) - Create Text Document
* [GetDocumentationFromKnowledgeBase](docs/sdks/agentsplatform/README.md#getdocumentationfromknowledgebase) - Get Documentation From Knowledge Base
* [DeleteKnowledgeBaseDocument](docs/sdks/agentsplatform/README.md#deleteknowledgebasedocument) - Delete Knowledge Base Document Or Folder
* [UpdateDocumentRoute](docs/sdks/agentsplatform/README.md#updatedocumentroute) - Update Document
* [GetRagIndexOverview](docs/sdks/agentsplatform/README.md#getragindexoverview) - Get Rag Index Overview.
* [GetOrCreateRagIndexes](docs/sdks/agentsplatform/README.md#getorcreateragindexes) - Compute Rag Indexes In Batch
* [RefreshURLDocumentRoute](docs/sdks/agentsplatform/README.md#refreshurldocumentroute) - Refresh Url Document Content
* [GetRagIndexes](docs/sdks/agentsplatform/README.md#getragindexes) - Get Rag Indexes Of The Specified Knowledgebase Document.
* [RagIndexStatus](docs/sdks/agentsplatform/README.md#ragindexstatus) - Compute Rag Index.
* [DeleteRagIndex](docs/sdks/agentsplatform/README.md#deleteragindex) - Delete Rag Index.
* [SearchKnowledgeBaseContentRoute](docs/sdks/agentsplatform/README.md#searchknowledgebasecontentroute) - Search Knowledge Base Content
* [GetKnowledgeBaseDependentAgents](docs/sdks/agentsplatform/README.md#getknowledgebasedependentagents) - Get Dependent Agents List
* [GetKnowledgeBaseContent](docs/sdks/agentsplatform/README.md#getknowledgebasecontent) - Get Document Content
* [GetKnowledgeBaseSourceFileURL](docs/sdks/agentsplatform/README.md#getknowledgebasesourcefileurl) - Get Document Source File Url
* [GetDocumentationChunkFromKnowledgeBase](docs/sdks/agentsplatform/README.md#getdocumentationchunkfromknowledgebase) - Get Documentation Chunk From Knowledge Base
* [GetToolsRoute](docs/sdks/agentsplatform/README.md#gettoolsroute) - Get Tools
* [AddToolRoute](docs/sdks/agentsplatform/README.md#addtoolroute) - Add Tool
* [GetToolRoute](docs/sdks/agentsplatform/README.md#gettoolroute) - Get Tool
* [DeleteToolRoute](docs/sdks/agentsplatform/README.md#deletetoolroute) - Delete Tool
* [UpdateToolRoute](docs/sdks/agentsplatform/README.md#updatetoolroute) - Update Tool
* [GetToolDependentAgentsRoute](docs/sdks/agentsplatform/README.md#gettooldependentagentsroute) - Get Dependent Agents List
* [GetSettingsRoute](docs/sdks/agentsplatform/README.md#getsettingsroute) - Get Convai Settings
* [UpdateSettingsRoute](docs/sdks/agentsplatform/README.md#updatesettingsroute) - Update Convai Settings
* [GetDashboardSettingsRoute](docs/sdks/agentsplatform/README.md#getdashboardsettingsroute) - Get Convai Dashboard Settings
* [UpdateDashboardSettingsRoute](docs/sdks/agentsplatform/README.md#updatedashboardsettingsroute) - Update Convai Dashboard Settings
* [GetSecretsRoute](docs/sdks/agentsplatform/README.md#getsecretsroute) - Get Convai Workspace Secrets
* [CreateSecretRoute](docs/sdks/agentsplatform/README.md#createsecretroute) - Create Convai Workspace Secret
* [DeleteSecretRoute](docs/sdks/agentsplatform/README.md#deletesecretroute) - Delete Convai Workspace Secret
* [UpdateSecretRoute](docs/sdks/agentsplatform/README.md#updatesecretroute) - Update Convai Workspace Secret
* [CreateBatchCall](docs/sdks/agentsplatform/README.md#createbatchcall) - Submit A Batch Call Request.
* [GetWorkspaceBatchCalls](docs/sdks/agentsplatform/README.md#getworkspacebatchcalls) - Get All Batch Calls For A Workspace.
* [GetBatchCall](docs/sdks/agentsplatform/README.md#getbatchcall) - Get A Batch Call By Id.
* [DeleteBatchCall](docs/sdks/agentsplatform/README.md#deletebatchcall) - Delete A Batch Call.
* [CancelBatchCall](docs/sdks/agentsplatform/README.md#cancelbatchcall) - Cancel A Batch Call.
* [RetryBatchCall](docs/sdks/agentsplatform/README.md#retrybatchcall) - Retry A Batch Call.
* [HandleSipTrunkOutboundCall](docs/sdks/agentsplatform/README.md#handlesiptrunkoutboundcall) - Handle An Outbound Call Via Sip Trunk
* [ListMcpServersRoute](docs/sdks/agentsplatform/README.md#listmcpserversroute) - List Mcp Servers
* [CreateMcpServerRoute](docs/sdks/agentsplatform/README.md#createmcpserverroute) - Create Mcp Server
* [GetMcpRoute](docs/sdks/agentsplatform/README.md#getmcproute) - Get Mcp Server
* [DeleteMcpServerRoute](docs/sdks/agentsplatform/README.md#deletemcpserverroute) - Delete Mcp Server
* [UpdateMcpServerConfigRoute](docs/sdks/agentsplatform/README.md#updatemcpserverconfigroute) - Update Mcp Server Configuration
* [ListMcpServerToolsRoute](docs/sdks/agentsplatform/README.md#listmcpservertoolsroute) - List Mcp Server Tools
* [~~UpdateMcpServerApprovalPolicyRoute~~](docs/sdks/agentsplatform/README.md#updatemcpserverapprovalpolicyroute) - Update Mcp Server Approval Policy :warning: **Deprecated**
* [AddMcpServerToolApprovalRoute](docs/sdks/agentsplatform/README.md#addmcpservertoolapprovalroute) - Create Mcp Server Tool Approval
* [RemoveMcpServerToolApprovalRoute](docs/sdks/agentsplatform/README.md#removemcpservertoolapprovalroute) - Delete Mcp Server Tool Approval
* [AddMcpToolConfigOverrideRoute](docs/sdks/agentsplatform/README.md#addmcptoolconfigoverrideroute) - Create Mcp Tool Configuration Override
* [GetMcpToolConfigOverrideRoute](docs/sdks/agentsplatform/README.md#getmcptoolconfigoverrideroute) - Get Mcp Tool Configuration Override
* [RemoveMcpToolConfigOverrideRoute](docs/sdks/agentsplatform/README.md#removemcptoolconfigoverrideroute) - Delete Mcp Tool Configuration Override
* [UpdateMcpToolConfigOverrideRoute](docs/sdks/agentsplatform/README.md#updatemcptoolconfigoverrideroute) - Update Mcp Tool Configuration Override
* [GetWhatsappAccount](docs/sdks/agentsplatform/README.md#getwhatsappaccount) - Get Whatsapp Account
* [DeleteWhatsappAccount](docs/sdks/agentsplatform/README.md#deletewhatsappaccount) - Delete Whatsapp Account
* [UpdateWhatsappAccount](docs/sdks/agentsplatform/README.md#updatewhatsappaccount) - Update Whatsapp Account
* [ListWhatsappAccounts](docs/sdks/agentsplatform/README.md#listwhatsappaccounts) - List Whatsapp Accounts
* [GetBranchesRoute](docs/sdks/agentsplatform/README.md#getbranchesroute) - List Agent Branches
* [CreateBranchRoute](docs/sdks/agentsplatform/README.md#createbranchroute) - Create A New Branch
* [GetBranchRoute](docs/sdks/agentsplatform/README.md#getbranchroute) - Get Agent Branch
* [UpdateBranchRoute](docs/sdks/agentsplatform/README.md#updatebranchroute) - Update Agent Branch
* [MergeBranchIntoTarget](docs/sdks/agentsplatform/README.md#mergebranchintotarget) - Merge A Branch Into A Target Branch
* [CreateAgentDeploymentRoute](docs/sdks/agentsplatform/README.md#createagentdeploymentroute) - Create Or Update Deployments
* [CreateAgentDraftRoute](docs/sdks/agentsplatform/README.md#createagentdraftroute) - Create Agent Draft
* [DeleteAgentDraftRoute](docs/sdks/agentsplatform/README.md#deleteagentdraftroute) - Delete Agent Draft
* [ListEnvironmentVariables](docs/sdks/agentsplatform/README.md#listenvironmentvariables) - List Environment Variables
* [CreateEnvironmentVariable](docs/sdks/agentsplatform/README.md#createenvironmentvariable) - Create Environment Variable
* [GetEnvironmentVariable](docs/sdks/agentsplatform/README.md#getenvironmentvariable) - Get Environment Variable
* [UpdateEnvironmentVariable](docs/sdks/agentsplatform/README.md#updateenvironmentvariable) - Update Environment Variable

### [AgentsWorkspaceAnalytics](docs/sdks/agentsworkspaceanalytics/README.md)

* [RunConversationAnalysis](docs/sdks/agentsworkspaceanalytics/README.md#runconversationanalysis) - Run Conversation Analysis

### [AudioIsolation](docs/sdks/audioisolation/README.md)

* [AudioIsolation](docs/sdks/audioisolation/README.md#audioisolation) - Audio Isolation
* [AudioIsolationStream](docs/sdks/audioisolation/README.md#audioisolationstream) - Audio Isolation Stream

### [AudioNative](docs/sdks/audionative/README.md)

* [CreateAudioNativeProject](docs/sdks/audionative/README.md#createaudionativeproject) - Creates Audio Native Enabled Project.
* [GetAudioNativeProjectSettingsEndpoint](docs/sdks/audionative/README.md#getaudionativeprojectsettingsendpoint) - Get Audio Native Project Settings
* [AudioNativeProjectUpdateContentEndpoint](docs/sdks/audionative/README.md#audionativeprojectupdatecontentendpoint) - Update Audio-Native Project Content
* [AudioNativeUpdateContentFromURL](docs/sdks/audionative/README.md#audionativeupdatecontentfromurl) - Update Audio-Native Content From Url

### [ConversationalAI](docs/sdks/conversationalai/README.md)

* [CreateFolderRoute](docs/sdks/conversationalai/README.md#createfolderroute) - Create Folder
* [PostKnowledgeBaseMoveRoute](docs/sdks/conversationalai/README.md#postknowledgebasemoveroute) - Move Entity To Folder
* [PostKnowledgeBaseBulkMoveRoute](docs/sdks/conversationalai/README.md#postknowledgebasebulkmoveroute) - Bulk Move Entities To Folder

### [Dubbing](docs/sdks/dubbing/README.md)

* [GetDubbingResource](docs/sdks/dubbing/README.md#getdubbingresource) - Get The Dubbing Resource For An Id.
* [AddLanguage](docs/sdks/dubbing/README.md#addlanguage) - Add A Language To The Resource
* [CreateClip](docs/sdks/dubbing/README.md#createclip) - Create A Segment For The Speaker
* [UpdateSegmentLanguage](docs/sdks/dubbing/README.md#updatesegmentlanguage) - Modify A Single Segment
* [MigrateSegments](docs/sdks/dubbing/README.md#migratesegments) - Move Segments Between Speakers
* [DeleteSegment](docs/sdks/dubbing/README.md#deletesegment) - Deletes A Single Segment
* [Transcribe](docs/sdks/dubbing/README.md#transcribe) - Transcribes Segments
* [Translate](docs/sdks/dubbing/README.md#translate) - Translates All Or Some Segments And Languages
* [Dub](docs/sdks/dubbing/README.md#dub) - Dubs All Or Some Segments And Languages
* [UpdateSpeaker](docs/sdks/dubbing/README.md#updatespeaker) - Update Metadata For A Speaker
* [CreateSpeaker](docs/sdks/dubbing/README.md#createspeaker) - Create A New Speaker
* [GetSimilarVoicesForSpeaker](docs/sdks/dubbing/README.md#getsimilarvoicesforspeaker) - Search The Elevenlabs Library For Voices Similar To A Speaker.
* [Render](docs/sdks/dubbing/README.md#render) - Render Audio Or Video For The Given Language
* [ListDubs](docs/sdks/dubbing/README.md#listdubs) - List Dubs
* [CreateDubbing](docs/sdks/dubbing/README.md#createdubbing) - Dub A Video Or An Audio File
* [GetDubbedMetadata](docs/sdks/dubbing/README.md#getdubbedmetadata) - Get Dubbing
* [DeleteDubbing](docs/sdks/dubbing/README.md#deletedubbing) - Delete Dubbing
* [GetDubbedFile](docs/sdks/dubbing/README.md#getdubbedfile) - Get Dubbed File
* [~~GetDubbedTranscriptFile~~](docs/sdks/dubbing/README.md#getdubbedtranscriptfile) - Get Dubbed Transcript :warning: **Deprecated**
* [GetDubbingTranscripts](docs/sdks/dubbing/README.md#getdubbingtranscripts) - Retrieve A Transcript

### [Enterprise](docs/sdks/enterprise/README.md)

* [GetDubbingResource](docs/sdks/enterprise/README.md#getdubbingresource) - Get The Dubbing Resource For An Id.
* [AddLanguage](docs/sdks/enterprise/README.md#addlanguage) - Add A Language To The Resource
* [CreateClip](docs/sdks/enterprise/README.md#createclip) - Create A Segment For The Speaker
* [UpdateSegmentLanguage](docs/sdks/enterprise/README.md#updatesegmentlanguage) - Modify A Single Segment
* [MigrateSegments](docs/sdks/enterprise/README.md#migratesegments) - Move Segments Between Speakers
* [DeleteSegment](docs/sdks/enterprise/README.md#deletesegment) - Deletes A Single Segment
* [Transcribe](docs/sdks/enterprise/README.md#transcribe) - Transcribes Segments
* [Translate](docs/sdks/enterprise/README.md#translate) - Translates All Or Some Segments And Languages
* [Dub](docs/sdks/enterprise/README.md#dub) - Dubs All Or Some Segments And Languages
* [UpdateSpeaker](docs/sdks/enterprise/README.md#updatespeaker) - Update Metadata For A Speaker
* [CreateSpeaker](docs/sdks/enterprise/README.md#createspeaker) - Create A New Speaker
* [GetSimilarVoicesForSpeaker](docs/sdks/enterprise/README.md#getsimilarvoicesforspeaker) - Search The Elevenlabs Library For Voices Similar To A Speaker.
* [Render](docs/sdks/enterprise/README.md#render) - Render Audio Or Video For The Given Language

### [ForcedAlignment](docs/sdks/forcedalignment/README.md)

* [ForcedAlignment](docs/sdks/forcedalignment/README.md#forcedalignment) - Create Forced Alignment

### [Models](docs/sdks/models/README.md)

* [GetModels](docs/sdks/models/README.md#getmodels) - Get Models

### [MusicGeneration](docs/sdks/musicgeneration/README.md)

* [ComposePlan](docs/sdks/musicgeneration/README.md#composeplan) - Generate Composition Plan
* [Generate](docs/sdks/musicgeneration/README.md#generate) - Compose Music
* [ComposeDetailed](docs/sdks/musicgeneration/README.md#composedetailed) - Compose Music With A Detailed Response
* [StreamCompose](docs/sdks/musicgeneration/README.md#streamcompose) - Stream Composed Music
* [UploadSong](docs/sdks/musicgeneration/README.md#uploadsong) - Upload Music
* [SeparateSongStems](docs/sdks/musicgeneration/README.md#separatesongstems) - Stem Separation

### [PronunciationDictionary](docs/sdks/pronunciationdictionary/README.md)

* [AddFromFile](docs/sdks/pronunciationdictionary/README.md#addfromfile) - Add A Pronunciation Dictionary
* [AddFromRules](docs/sdks/pronunciationdictionary/README.md#addfromrules) - Add A Pronunciation Dictionary
* [GetPronunciationDictionaryMetadata](docs/sdks/pronunciationdictionary/README.md#getpronunciationdictionarymetadata) - Get Metadata For A Pronunciation Dictionary
* [PatchPronunciationDictionary](docs/sdks/pronunciationdictionary/README.md#patchpronunciationdictionary) - Update Pronunciation Dictionary
* [SetRules](docs/sdks/pronunciationdictionary/README.md#setrules) - Set Rules On The Pronunciation Dictionary
* [AddRules](docs/sdks/pronunciationdictionary/README.md#addrules) - Add Rules To The Pronunciation Dictionary
* [RemoveRules](docs/sdks/pronunciationdictionary/README.md#removerules) - Remove Rules From The Pronunciation Dictionary
* [GetPronunciationDictionaryVersionPls](docs/sdks/pronunciationdictionary/README.md#getpronunciationdictionaryversionpls) - Get A Pls File With A Pronunciation Dictionary Version Rules
* [GetPronunciationDictionariesMetadata](docs/sdks/pronunciationdictionary/README.md#getpronunciationdictionariesmetadata) - Get Pronunciation Dictionaries

### [PvcVoices](docs/sdks/pvcvoices/README.md)

* [CreatePvcVoice](docs/sdks/pvcvoices/README.md#createpvcvoice) - Create Pvc Voice
* [EditPvcVoice](docs/sdks/pvcvoices/README.md#editpvcvoice) - Edit Pvc Voice
* [AddPvcVoiceSamples](docs/sdks/pvcvoices/README.md#addpvcvoicesamples) - Add Samples To Pvc Voice
* [EditPvcVoiceSample](docs/sdks/pvcvoices/README.md#editpvcvoicesample) - Update Pvc Voice Sample
* [DeletePvcVoiceSample](docs/sdks/pvcvoices/README.md#deletepvcvoicesample) - Delete Pvc Voice Sample
* [GetPvcSampleAudio](docs/sdks/pvcvoices/README.md#getpvcsampleaudio) - Retrieve Voice Sample Audio
* [GetPvcSampleVisualWaveform](docs/sdks/pvcvoices/README.md#getpvcsamplevisualwaveform) - Retrieve Voice Sample Visual Waveform
* [GetPvcSampleSpeakers](docs/sdks/pvcvoices/README.md#getpvcsamplespeakers) - Retrieve Speaker Separation Status
* [StartSpeakerSeparation](docs/sdks/pvcvoices/README.md#startspeakerseparation) - Start Speaker Separation
* [GetSpeakerAudio](docs/sdks/pvcvoices/README.md#getspeakeraudio) - Retrieve Separated Speaker Audio
* [GetPvcVoiceCaptcha](docs/sdks/pvcvoices/README.md#getpvcvoicecaptcha) - Get Pvc Voice Captcha
* [VerifyPvcVoiceCaptcha](docs/sdks/pvcvoices/README.md#verifypvcvoicecaptcha) - Verify Pvc Voice Captcha
* [RunPvcVoiceTraining](docs/sdks/pvcvoices/README.md#runpvcvoicetraining) - Run Pvc Training
* [RequestPvcManualVerification](docs/sdks/pvcvoices/README.md#requestpvcmanualverification) - Request Manual Verification

### [Resource](docs/sdks/resource/README.md)

* [GetDubbingResource](docs/sdks/resource/README.md#getdubbingresource) - Get The Dubbing Resource For An Id.
* [AddLanguage](docs/sdks/resource/README.md#addlanguage) - Add A Language To The Resource
* [CreateClip](docs/sdks/resource/README.md#createclip) - Create A Segment For The Speaker
* [UpdateSegmentLanguage](docs/sdks/resource/README.md#updatesegmentlanguage) - Modify A Single Segment
* [MigrateSegments](docs/sdks/resource/README.md#migratesegments) - Move Segments Between Speakers
* [DeleteSegment](docs/sdks/resource/README.md#deletesegment) - Deletes A Single Segment
* [Transcribe](docs/sdks/resource/README.md#transcribe) - Transcribes Segments
* [Translate](docs/sdks/resource/README.md#translate) - Translates All Or Some Segments And Languages
* [Dub](docs/sdks/resource/README.md#dub) - Dubs All Or Some Segments And Languages
* [UpdateSpeaker](docs/sdks/resource/README.md#updatespeaker) - Update Metadata For A Speaker
* [CreateSpeaker](docs/sdks/resource/README.md#createspeaker) - Create A New Speaker
* [GetSimilarVoicesForSpeaker](docs/sdks/resource/README.md#getsimilarvoicesforspeaker) - Search The Elevenlabs Library For Voices Similar To A Speaker.
* [Render](docs/sdks/resource/README.md#render) - Render Audio Or Video For The Given Language

### [Samples](docs/sdks/samples/README.md)

* [DeleteSample](docs/sdks/samples/README.md#deletesample) - Delete Sample
* [GetAudioFromSample](docs/sdks/samples/README.md#getaudiofromsample) - Get Audio From Sample

### [Segment](docs/sdks/segment/README.md)

* [GetDubbingResource](docs/sdks/segment/README.md#getdubbingresource) - Get The Dubbing Resource For An Id.
* [AddLanguage](docs/sdks/segment/README.md#addlanguage) - Add A Language To The Resource
* [CreateClip](docs/sdks/segment/README.md#createclip) - Create A Segment For The Speaker
* [UpdateSegmentLanguage](docs/sdks/segment/README.md#updatesegmentlanguage) - Modify A Single Segment
* [MigrateSegments](docs/sdks/segment/README.md#migratesegments) - Move Segments Between Speakers
* [DeleteSegment](docs/sdks/segment/README.md#deletesegment) - Deletes A Single Segment
* [Transcribe](docs/sdks/segment/README.md#transcribe) - Transcribes Segments
* [Translate](docs/sdks/segment/README.md#translate) - Translates All Or Some Segments And Languages
* [Dub](docs/sdks/segment/README.md#dub) - Dubs All Or Some Segments And Languages
* [UpdateSpeaker](docs/sdks/segment/README.md#updatespeaker) - Update Metadata For A Speaker
* [CreateSpeaker](docs/sdks/segment/README.md#createspeaker) - Create A New Speaker
* [GetSimilarVoicesForSpeaker](docs/sdks/segment/README.md#getsimilarvoicesforspeaker) - Search The Elevenlabs Library For Voices Similar To A Speaker.
* [Render](docs/sdks/segment/README.md#render) - Render Audio Or Video For The Given Language

### [SingleUseToken](docs/sdks/singleusetoken/README.md)

* [GetSingleUseToken](docs/sdks/singleusetoken/README.md#getsingleusetoken) - Create Single Use Token

### [SoundGeneration](docs/sdks/soundgeneration/README.md)

* [SoundGeneration](docs/sdks/soundgeneration/README.md#soundgeneration) - Sound Generation

### [SpeechHistory](docs/sdks/speechhistory/README.md)

* [GetSpeechHistory](docs/sdks/speechhistory/README.md#getspeechhistory) - List Generated Items
* [GetSpeechHistoryItemByID](docs/sdks/speechhistory/README.md#getspeechhistoryitembyid) - Get History Item
* [DeleteSpeechHistoryItem](docs/sdks/speechhistory/README.md#deletespeechhistoryitem) - Delete History Item
* [GetAudioFullFromSpeechHistoryItem](docs/sdks/speechhistory/README.md#getaudiofullfromspeechhistoryitem) - Get Audio From History Item
* [DownloadSpeechHistoryItems](docs/sdks/speechhistory/README.md#downloadspeechhistoryitems) - Download History Items

### [SpeechToSpeech](docs/sdks/speechtospeech/README.md)

* [SpeechToSpeechFull](docs/sdks/speechtospeech/README.md#speechtospeechfull) - Speech To Speech
* [SpeechToSpeechStream](docs/sdks/speechtospeech/README.md#speechtospeechstream) - Speech To Speech Streaming

### [SpeechToText](docs/sdks/speechtotext/README.md)

* [SpeechToText](docs/sdks/speechtotext/README.md#speechtotext) - Speech To Text
* [GetTranscriptByID](docs/sdks/speechtotext/README.md#gettranscriptbyid) - Get Transcript By Id
* [DeleteTranscriptByID](docs/sdks/speechtotext/README.md#deletetranscriptbyid) - Delete Transcript By Id

### [Studio](docs/sdks/studio/README.md)

* [CreatePodcast](docs/sdks/studio/README.md#createpodcast) - Create Podcast
* [UpdatePronunciationDictionaries](docs/sdks/studio/README.md#updatepronunciationdictionaries) - Create Pronunciation Dictionaries
* [GetProjects](docs/sdks/studio/README.md#getprojects) - List Studio Projects
* [AddProject](docs/sdks/studio/README.md#addproject) - Create Studio Project
* [GetProjectByID](docs/sdks/studio/README.md#getprojectbyid) - Get Studio Project
* [EditProject](docs/sdks/studio/README.md#editproject) - Update Studio Project
* [DeleteProject](docs/sdks/studio/README.md#deleteproject) - Delete Studio Project
* [EditProjectContent](docs/sdks/studio/README.md#editprojectcontent) - Update Studio Project Content
* [ConvertProjectEndpoint](docs/sdks/studio/README.md#convertprojectendpoint) - Convert Studio Project
* [GetProjectSnapshots](docs/sdks/studio/README.md#getprojectsnapshots) - List Studio Project Snapshots
* [GetProjectSnapshotEndpoint](docs/sdks/studio/README.md#getprojectsnapshotendpoint) - Get Project Snapshot
* [StreamProjectSnapshotAudioEndpoint](docs/sdks/studio/README.md#streamprojectsnapshotaudioendpoint) - Stream Studio Project Audio
* [StreamProjectSnapshotArchiveEndpoint](docs/sdks/studio/README.md#streamprojectsnapshotarchiveendpoint) - Stream Archive With Studio Project Audio
* [GetChapters](docs/sdks/studio/README.md#getchapters) - List Chapters
* [AddChapter](docs/sdks/studio/README.md#addchapter) - Create Chapter
* [GetChapterByIDEndpoint](docs/sdks/studio/README.md#getchapterbyidendpoint) - Get Chapter
* [EditChapter](docs/sdks/studio/README.md#editchapter) - Update Chapter
* [DeleteChapterEndpoint](docs/sdks/studio/README.md#deletechapterendpoint) - Delete Chapter
* [ConvertChapterEndpoint](docs/sdks/studio/README.md#convertchapterendpoint) - Convert Chapter
* [GetChapterSnapshots](docs/sdks/studio/README.md#getchaptersnapshots) - List Chapter Snapshots
* [GetChapterSnapshotEndpoint](docs/sdks/studio/README.md#getchaptersnapshotendpoint) - Get Chapter Snapshot
* [StreamChapterSnapshotAudio](docs/sdks/studio/README.md#streamchaptersnapshotaudio) - Stream Chapter Audio
* [GetProjectMutedTracksEndpoint](docs/sdks/studio/README.md#getprojectmutedtracksendpoint) - Get Project Muted Tracks

### [TextToDialogue](docs/sdks/texttodialogue/README.md)

* [TextToDialogue](docs/sdks/texttodialogue/README.md#texttodialogue) - Text To Dialogue (Multi-Voice)
* [TextToDialogueStream](docs/sdks/texttodialogue/README.md#texttodialoguestream) - Text To Dialogue (Multi-Voice) Streaming
* [TextToDialogueStreamWithTimestamps](docs/sdks/texttodialogue/README.md#texttodialoguestreamwithtimestamps) - Text To Dialogue Streaming With Timestamps
* [TextToDialogueFullWithTimestamps](docs/sdks/texttodialogue/README.md#texttodialoguefullwithtimestamps) - Text To Dialogue With Timestamps

### [TextToSpeech](docs/sdks/texttospeech/README.md)

* [TextToSpeechFull](docs/sdks/texttospeech/README.md#texttospeechfull) - Text To Speech
* [TextToSpeechFullWithTimestamps](docs/sdks/texttospeech/README.md#texttospeechfullwithtimestamps) - Text To Speech With Timestamps
* [TextToSpeechStream](docs/sdks/texttospeech/README.md#texttospeechstream) - Text To Speech Streaming
* [TextToSpeechStreamWithTimestamps](docs/sdks/texttospeech/README.md#texttospeechstreamwithtimestamps) - Text To Speech Streaming With Timestamps

### [TextToVoice](docs/sdks/texttovoice/README.md)

* [TextToVoice](docs/sdks/texttovoice/README.md#texttovoice) - Generate A Voice Preview From Description
* [CreateVoice](docs/sdks/texttovoice/README.md#createvoice) - Create A New Voice From Voice Preview
* [TextToVoiceDesign](docs/sdks/texttovoice/README.md#texttovoicedesign) - Design A Voice.
* [TextToVoiceRemix](docs/sdks/texttovoice/README.md#texttovoiceremix) - Remix A Voice.
* [TextToVoicePreviewStream](docs/sdks/texttovoice/README.md#texttovoicepreviewstream) - Text To Voice Preview Streaming

### [VideoToMusic](docs/sdks/videotomusic/README.md)

* [VideoToMusic](docs/sdks/videotomusic/README.md#videotomusic) - Video To Music

### [Voices](docs/sdks/voices/README.md)

* [GetVoices](docs/sdks/voices/README.md#getvoices) - List Voices
* [GetUserVoicesV2](docs/sdks/voices/README.md#getuservoicesv2) - Get Voices V2
* [GetVoiceSettingsDefault](docs/sdks/voices/README.md#getvoicesettingsdefault) - Get Default Voice Settings.
* [GetVoiceSettings](docs/sdks/voices/README.md#getvoicesettings) - Get Voice Settings
* [GetVoiceByID](docs/sdks/voices/README.md#getvoicebyid) - Get Voice
* [DeleteVoice](docs/sdks/voices/README.md#deletevoice) - Delete Voice
* [EditVoiceSettings](docs/sdks/voices/README.md#editvoicesettings) - Edit Voice Settings
* [AddVoice](docs/sdks/voices/README.md#addvoice) - Add Voice
* [EditVoice](docs/sdks/voices/README.md#editvoice) - Edit Voice
* [AddSharingVoice](docs/sdks/voices/README.md#addsharingvoice) - Add Shared Voice
* [GetLibraryVoices](docs/sdks/voices/README.md#getlibraryvoices) - Get Voices
* [GetSimilarLibraryVoices](docs/sdks/voices/README.md#getsimilarlibraryvoices) - Get Similar Library Voices

### [Workspace](docs/sdks/workspace/README.md)

* [GetServiceAccountAPIKeysRoute](docs/sdks/workspace/README.md#getserviceaccountapikeysroute) - Get Service Account Api Keys Route
* [CreateServiceAccountAPIKey](docs/sdks/workspace/README.md#createserviceaccountapikey) - Create Service Account Api Key
* [DeleteServiceAccountAPIKey](docs/sdks/workspace/README.md#deleteserviceaccountapikey) - Delete Service Account Api Key
* [EditServiceAccountAPIKey](docs/sdks/workspace/README.md#editserviceaccountapikey) - Edit Service Account Api Key
* [ListAuthConnections](docs/sdks/workspace/README.md#listauthconnections) - Get Workspace Auth Connections
* [CreateAuthConnection](docs/sdks/workspace/README.md#createauthconnection) - Create Workspace Auth Connection
* [DeleteAuthConnection](docs/sdks/workspace/README.md#deleteauthconnection) - Delete Workspace Auth Connection
* [GetWorkspaceServiceAccounts](docs/sdks/workspace/README.md#getworkspaceserviceaccounts) - Get Workspace Service Accounts
* [GetGroupsEndpoint](docs/sdks/workspace/README.md#getgroupsendpoint) - Get All Groups
* [SearchGroups](docs/sdks/workspace/README.md#searchgroups) - Search User Groups
* [RemoveMember](docs/sdks/workspace/README.md#removemember) - Delete Member From User Group
* [AddMember](docs/sdks/workspace/README.md#addmember) - Add Member To User Group
* [InviteUser](docs/sdks/workspace/README.md#inviteuser) - Invite User
* [InviteUsersBulk](docs/sdks/workspace/README.md#inviteusersbulk) - Invite Multiple Users
* [DeleteInvite](docs/sdks/workspace/README.md#deleteinvite) - Delete Existing Invitation
* [UpdateWorkspaceMember](docs/sdks/workspace/README.md#updateworkspacemember) - Update Member
* [GetResourceMetadata](docs/sdks/workspace/README.md#getresourcemetadata) - Get Resource
* [ShareResourceEndpoint](docs/sdks/workspace/README.md#shareresourceendpoint) - Share Workspace Resource
* [UnshareResourceEndpoint](docs/sdks/workspace/README.md#unshareresourceendpoint) - Unshare Workspace Resource
* [GetWorkspaceWebhooksRoute](docs/sdks/workspace/README.md#getworkspacewebhooksroute) - List Workspace Webhooks
* [CreateWorkspaceWebhookRoute](docs/sdks/workspace/README.md#createworkspacewebhookroute) - Create Workspace Webhook
* [DeleteWorkspaceWebhookRoute](docs/sdks/workspace/README.md#deleteworkspacewebhookroute) - Delete Workspace Webhook
* [EditWorkspaceWebhookRoute](docs/sdks/workspace/README.md#editworkspacewebhookroute) - Update Workspace Webhook

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries. If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API. However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a `retry.Config` object to the call by using the `WithRetries` option:
```go
package main

import (
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/retry"
	"log"
	"models/operations"
)

func main() {
	ctx := context.Background()

	s := elevenlabsgo.New(
		"https://api.example.com",
		elevenlabsgo.WithSecurity("YOUR_API_KEY"),
	)

	res, err := s.GetUserSubscriptionInfo(ctx, optionalnullable.From[string](nil), operations.WithRetries(
		retry.Config{
			Strategy: "backoff",
			Backoff: &retry.BackoffStrategy{
				InitialInterval: 1,
				MaxInterval:     50,
				Exponent:        1.1,
				MaxElapsedTime:  100,
			},
			RetryConnectionErrors: false,
		}))
	if err != nil {
		log.Fatal(err)
	}
	if res.ExtendedSubscriptionResponseModel != nil {
		switch res.ExtendedSubscriptionResponseModel.PendingChange.Type {
		case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingSubscriptionSwitchResponseModel is populated
		case components.PendingChangeTypePendingCancellationResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingCancellationResponseModel is populated
		}

	}
}

```

If you'd like to override the default retry strategy for all operations that support retries, you can use the `WithRetryConfig` option at SDK initialization:
```go
package main

import (
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"github.com/bdlilley/elevenlabs-go/retry"
	"log"
)

func main() {
	ctx := context.Background()

	s := elevenlabsgo.New(
		"https://api.example.com",
		elevenlabsgo.WithRetryConfig(
			retry.Config{
				Strategy: "backoff",
				Backoff: &retry.BackoffStrategy{
					InitialInterval: 1,
					MaxInterval:     50,
					Exponent:        1.1,
					MaxElapsedTime:  100,
				},
				RetryConnectionErrors: false,
			}),
		elevenlabsgo.WithSecurity("YOUR_API_KEY"),
	)

	res, err := s.GetUserSubscriptionInfo(ctx, optionalnullable.From[string](nil))
	if err != nil {
		log.Fatal(err)
	}
	if res.ExtendedSubscriptionResponseModel != nil {
		switch res.ExtendedSubscriptionResponseModel.PendingChange.Type {
		case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingSubscriptionSwitchResponseModel is populated
		case components.PendingChangeTypePendingCancellationResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingCancellationResponseModel is populated
		}

	}
}

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

Handling errors in this SDK should largely match your expectations. All operations return a response object or an error, they will never return both.

By Default, an API error will return `apierrors.APIError`. When custom error responses are specified for an operation, the SDK may also return their associated error. You can refer to respective *Errors* tables in SDK docs for more details on possible error types for each operation.

For example, the `GetUserSubscriptionInfo` function may return the following errors:

| Error Type                    | Status Code | Content Type     |
| ----------------------------- | ----------- | ---------------- |
| apierrors.HTTPValidationError | 422         | application/json |
| apierrors.APIError            | 4XX, 5XX    | \*/\*            |

### Example

```go
package main

import (
	"context"
	"errors"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/apierrors"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
	ctx := context.Background()

	s := elevenlabsgo.New(
		"https://api.example.com",
		elevenlabsgo.WithSecurity("YOUR_API_KEY"),
	)

	res, err := s.GetUserSubscriptionInfo(ctx, optionalnullable.From[string](nil))
	if err != nil {

		var e *apierrors.HTTPValidationError
		if errors.As(err, &e) {
			// handle error
			log.Fatal(e.Error())
		}

		var e *apierrors.APIError
		if errors.As(err, &e) {
			// handle error
			log.Fatal(e.Error())
		}
	}
}

```
<!-- End Error Handling [errors] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The Go SDK makes API calls that wrap an internal HTTP client. The requirements for the HTTP client are very simple. It must match this interface:

```go
type HTTPClient interface {
	Do(req *http.Request) (*http.Response, error)
}
```

The built-in `net/http` client satisfies this interface and a default client based on the built-in is provided by default. To replace this default with a client of your own, you can implement this interface yourself or provide your own client configured as desired. Here's a simple example, which adds a client with a 30 second timeout.

```go
import (
	"net/http"
	"time"

	"github.com/bdlilley/elevenlabs-go"
)

var (
	httpClient = &http.Client{Timeout: 30 * time.Second}
	sdkClient  = elevenlabsgo.New(elevenlabsgo.WithClient(httpClient))
)
```

This can be a convenient way to configure timeouts, cookies, proxies, custom headers, and other low-level configuration.
<!-- End Custom HTTP Client [http-client] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=elevenlabs-go&utm_campaign=go)
