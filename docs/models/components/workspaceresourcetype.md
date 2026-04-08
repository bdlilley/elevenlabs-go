# WorkspaceResourceType

Resource types that can be shared in the workspace. The name always need to match the collection names

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.WorkspaceResourceTypeVoice

// Open enum: custom values can be created with a direct type cast
custom := components.WorkspaceResourceType("custom_value")
```


## Values

| Name                                                          | Value                                                         |
| ------------------------------------------------------------- | ------------------------------------------------------------- |
| `WorkspaceResourceTypeVoice`                                  | voice                                                         |
| `WorkspaceResourceTypeVoiceCollection`                        | voice_collection                                              |
| `WorkspaceResourceTypePronunciationDictionary`                | pronunciation_dictionary                                      |
| `WorkspaceResourceTypeDubbing`                                | dubbing                                                       |
| `WorkspaceResourceTypeProject`                                | project                                                       |
| `WorkspaceResourceTypeConvaiAgents`                           | convai_agents                                                 |
| `WorkspaceResourceTypeConvaiKnowledgeBaseDocuments`           | convai_knowledge_base_documents                               |
| `WorkspaceResourceTypeConvaiTools`                            | convai_tools                                                  |
| `WorkspaceResourceTypeConvaiSettings`                         | convai_settings                                               |
| `WorkspaceResourceTypeConvaiSecrets`                          | convai_secrets                                                |
| `WorkspaceResourceTypeWorkspaceAuthConnections`               | workspace_auth_connections                                    |
| `WorkspaceResourceTypeConvaiPhoneNumbers`                     | convai_phone_numbers                                          |
| `WorkspaceResourceTypeConvaiMcpServers`                       | convai_mcp_servers                                            |
| `WorkspaceResourceTypeConvaiAPIIntegrationConnections`        | convai_api_integration_connections                            |
| `WorkspaceResourceTypeConvaiAPIIntegrationTriggerConnections` | convai_api_integration_trigger_connections                    |
| `WorkspaceResourceTypeConvaiBatchCalls`                       | convai_batch_calls                                            |
| `WorkspaceResourceTypeConvaiAgentResponseTests`               | convai_agent_response_tests                                   |
| `WorkspaceResourceTypeConvaiTestSuiteInvocations`             | convai_test_suite_invocations                                 |
| `WorkspaceResourceTypeConvaiCrawlJobs`                        | convai_crawl_jobs                                             |
| `WorkspaceResourceTypeConvaiCrawlTasks`                       | convai_crawl_tasks                                            |
| `WorkspaceResourceTypeConvaiWhatsappAccounts`                 | convai_whatsapp_accounts                                      |
| `WorkspaceResourceTypeConvaiAgentVersions`                    | convai_agent_versions                                         |
| `WorkspaceResourceTypeConvaiAgentBranches`                    | convai_agent_branches                                         |
| `WorkspaceResourceTypeConvaiAgentVersionsDeployments`         | convai_agent_versions_deployments                             |
| `WorkspaceResourceTypeConvaiMemoryEntries`                    | convai_memory_entries                                         |
| `WorkspaceResourceTypeConvaiCoachingProposals`                | convai_coaching_proposals                                     |
| `WorkspaceResourceTypeDashboard`                              | dashboard                                                     |
| `WorkspaceResourceTypeDashboardConfiguration`                 | dashboard_configuration                                       |
| `WorkspaceResourceTypeConvaiAgentDrafts`                      | convai_agent_drafts                                           |
| `WorkspaceResourceTypeResourceLocators`                       | resource_locators                                             |
| `WorkspaceResourceTypeAssets`                                 | assets                                                        |
| `WorkspaceResourceTypeContentGenerations`                     | content_generations                                           |
| `WorkspaceResourceTypeContentTemplates`                       | content_templates                                             |
| `WorkspaceResourceTypeSongs`                                  | songs                                                         |
| `WorkspaceResourceTypeAvatars`                                | avatars                                                       |
| `WorkspaceResourceTypeAvatarVideoGenerations`                 | avatar_video_generations                                      |