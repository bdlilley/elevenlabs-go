# PermissionType

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.PermissionTypeTextToSpeech

// Open enum: custom values can be created with a direct type cast
custom := components.PermissionType("custom_value")
```


## Values

| Name                                           | Value                                          |
| ---------------------------------------------- | ---------------------------------------------- |
| `PermissionTypeTextToSpeech`                   | text_to_speech                                 |
| `PermissionTypeSpeechToSpeech`                 | speech_to_speech                               |
| `PermissionTypeSpeechToText`                   | speech_to_text                                 |
| `PermissionTypeModelsRead`                     | models_read                                    |
| `PermissionTypeModelsWrite`                    | models_write                                   |
| `PermissionTypeVoicesRead`                     | voices_read                                    |
| `PermissionTypeVoicesWrite`                    | voices_write                                   |
| `PermissionTypeSpeechHistoryRead`              | speech_history_read                            |
| `PermissionTypeSpeechHistoryWrite`             | speech_history_write                           |
| `PermissionTypeSoundGeneration`                | sound_generation                               |
| `PermissionTypeAudioIsolation`                 | audio_isolation                                |
| `PermissionTypeVoiceGeneration`                | voice_generation                               |
| `PermissionTypeDubbingRead`                    | dubbing_read                                   |
| `PermissionTypeDubbingWrite`                   | dubbing_write                                  |
| `PermissionTypePronunciationDictionariesRead`  | pronunciation_dictionaries_read                |
| `PermissionTypePronunciationDictionariesWrite` | pronunciation_dictionaries_write               |
| `PermissionTypeUserRead`                       | user_read                                      |
| `PermissionTypeUserWrite`                      | user_write                                     |
| `PermissionTypeProjectsRead`                   | projects_read                                  |
| `PermissionTypeProjectsWrite`                  | projects_write                                 |
| `PermissionTypeAudioNativeRead`                | audio_native_read                              |
| `PermissionTypeAudioNativeWrite`               | audio_native_write                             |
| `PermissionTypeWorkspaceRead`                  | workspace_read                                 |
| `PermissionTypeWorkspaceWrite`                 | workspace_write                                |
| `PermissionTypeForcedAlignment`                | forced_alignment                               |
| `PermissionTypeConvaiRead`                     | convai_read                                    |
| `PermissionTypeConvaiWrite`                    | convai_write                                   |
| `PermissionTypeMusicGeneration`                | music_generation                               |
| `PermissionTypeImageVideoGeneration`           | image_video_generation                         |
| `PermissionTypeAddVoiceFromVoiceLibrary`       | add_voice_from_voice_library                   |
| `PermissionTypeCreateInstantVoiceClone`        | create_instant_voice_clone                     |
| `PermissionTypeCreateProfessionalVoiceClone`   | create_professional_voice_clone                |
| `PermissionTypePublishVoiceToVoiceLibrary`     | publish_voice_to_voice_library                 |
| `PermissionTypeShareVoiceExternally`           | share_voice_externally                         |
| `PermissionTypeCreateUserAPIKey`               | create_user_api_key                            |
| `PermissionTypeWorkspaceAnalyticsFullRead`     | workspace_analytics_full_read                  |
| `PermissionTypeWebhooksWrite`                  | webhooks_write                                 |
| `PermissionTypeServiceAccountWrite`            | service_account_write                          |
| `PermissionTypeGroupMembersManage`             | group_members_manage                           |
| `PermissionTypeWorkspaceMembersRead`           | workspace_members_read                         |
| `PermissionTypeWorkspaceMembersInvite`         | workspace_members_invite                       |
| `PermissionTypeWorkspaceMembersRemove`         | workspace_members_remove                       |
| `PermissionTypeTermsOfServiceAccept`           | terms_of_service_accept                        |
| `PermissionTypeAuditLogRead`                   | audit_log_read                                 |
| `PermissionTypeCopyResourcesCrossWorkspace`    | copy_resources_cross_workspace                 |