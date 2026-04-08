# PromptAgentAPIModelOutputBackupLlmConfig

Configuration for backup LLM cascading. Can be disabled, use system defaults, or specify custom order.


## Supported Types

### BackupLLMDefault

```go
promptAgentAPIModelOutputBackupLlmConfig := components.CreatePromptAgentAPIModelOutputBackupLlmConfigDefault(components.BackupLLMDefault{/* values here */})
```

### BackupLLMDisabled

```go
promptAgentAPIModelOutputBackupLlmConfig := components.CreatePromptAgentAPIModelOutputBackupLlmConfigDisabled(components.BackupLLMDisabled{/* values here */})
```

### BackupLLMOverride

```go
promptAgentAPIModelOutputBackupLlmConfig := components.CreatePromptAgentAPIModelOutputBackupLlmConfigOverride(components.BackupLLMOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelOutputBackupLlmConfig.Type {
	case components.PromptAgentAPIModelOutputBackupLlmConfigTypeDefault:
		// promptAgentAPIModelOutputBackupLlmConfig.BackupLLMDefault is populated
	case components.PromptAgentAPIModelOutputBackupLlmConfigTypeDisabled:
		// promptAgentAPIModelOutputBackupLlmConfig.BackupLLMDisabled is populated
	case components.PromptAgentAPIModelOutputBackupLlmConfigTypeOverride:
		// promptAgentAPIModelOutputBackupLlmConfig.BackupLLMOverride is populated
	default:
		// Unknown type - use promptAgentAPIModelOutputBackupLlmConfig.GetUnknownRaw() for raw JSON
}
```
