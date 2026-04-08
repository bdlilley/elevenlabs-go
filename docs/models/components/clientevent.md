# ClientEvent

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ClientEventConversationInitiationMetadata

// Open enum: custom values can be created with a direct type cast
custom := components.ClientEvent("custom_value")
```


## Values

| Name                                        | Value                                       |
| ------------------------------------------- | ------------------------------------------- |
| `ClientEventConversationInitiationMetadata` | conversation_initiation_metadata            |
| `ClientEventAsrInitiationMetadata`          | asr_initiation_metadata                     |
| `ClientEventPing`                           | ping                                        |
| `ClientEventAudio`                          | audio                                       |
| `ClientEventInterruption`                   | interruption                                |
| `ClientEventUserTranscript`                 | user_transcript                             |
| `ClientEventTentativeUserTranscript`        | tentative_user_transcript                   |
| `ClientEventAgentResponse`                  | agent_response                              |
| `ClientEventAgentResponseCorrection`        | agent_response_correction                   |
| `ClientEventClientToolCall`                 | client_tool_call                            |
| `ClientEventMcpToolCall`                    | mcp_tool_call                               |
| `ClientEventMcpConnectionStatus`            | mcp_connection_status                       |
| `ClientEventAgentToolRequest`               | agent_tool_request                          |
| `ClientEventAgentToolResponse`              | agent_tool_response                         |
| `ClientEventAgentResponseMetadata`          | agent_response_metadata                     |
| `ClientEventVadScore`                       | vad_score                                   |
| `ClientEventAgentChatResponsePart`          | agent_chat_response_part                    |
| `ClientEventClientError`                    | client_error                                |
| `ClientEventGuardrailTriggered`             | guardrail_triggered                         |
| `ClientEventDtmfRequest`                    | dtmf_request                                |
| `ClientEventInternalTurnProbability`        | internal_turn_probability                   |
| `ClientEventInternalTentativeAgentResponse` | internal_tentative_agent_response           |