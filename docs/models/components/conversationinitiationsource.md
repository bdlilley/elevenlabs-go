# ConversationInitiationSource

Enum representing the possible sources for conversation initiation.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ConversationInitiationSourceUnknown

// Open enum: custom values can be created with a direct type cast
custom := components.ConversationInitiationSource("custom_value")
```


## Values

| Name                                             | Value                                            |
| ------------------------------------------------ | ------------------------------------------------ |
| `ConversationInitiationSourceUnknown`            | unknown                                          |
| `ConversationInitiationSourceAndroidSDK`         | android_sdk                                      |
| `ConversationInitiationSourceNodeJsSDK`          | node_js_sdk                                      |
| `ConversationInitiationSourceReactNativeSDK`     | react_native_sdk                                 |
| `ConversationInitiationSourceReactSDK`           | react_sdk                                        |
| `ConversationInitiationSourceJsSDK`              | js_sdk                                           |
| `ConversationInitiationSourcePythonSDK`          | python_sdk                                       |
| `ConversationInitiationSourceWidget`             | widget                                           |
| `ConversationInitiationSourceSipTrunk`           | sip_trunk                                        |
| `ConversationInitiationSourceTwilio`             | twilio                                           |
| `ConversationInitiationSourceGenesys`            | genesys                                          |
| `ConversationInitiationSourceSwiftSDK`           | swift_sdk                                        |
| `ConversationInitiationSourceWhatsapp`           | whatsapp                                         |
| `ConversationInitiationSourceFlutterSDK`         | flutter_sdk                                      |
| `ConversationInitiationSourceZendeskIntegration` | zendesk_integration                              |
| `ConversationInitiationSourceSlackIntegration`   | slack_integration                                |
| `ConversationInitiationSourceTemplatePreview`    | template_preview                                 |