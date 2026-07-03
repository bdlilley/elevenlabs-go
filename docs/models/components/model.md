# Model

LLM model to use for custom guardrail evaluation

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ModelGemini25FlashLite

// Open enum: custom values can be created with a direct type cast
custom := components.Model("custom_value")
```


## Values

| Name                     | Value                    |
| ------------------------ | ------------------------ |
| `ModelGemini25FlashLite` | gemini-2.5-flash-lite    |
| `ModelGemini25Flash`     | gemini-2.5-flash         |
| `ModelGemini31FlashLite` | gemini-3.1-flash-lite    |
| `ModelGemini35Flash`     | gemini-3.5-flash         |
| `ModelClaudeHaiku45`     | claude-haiku-4-5         |
| `ModelClaudeSonnet46`    | claude-sonnet-4-6        |
| `ModelGpt54Nano`         | gpt-5.4-nano             |
| `ModelGpt54Mini`         | gpt-5.4-mini             |