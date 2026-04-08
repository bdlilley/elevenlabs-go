# PromptAgentAPIModelInputBackupLlmConfig

Configuration for backup LLM cascading. Can be disabled, use system defaults, or specify custom order.


## Supported Types

### BackupLLMDefault

```go
promptAgentAPIModelInputBackupLlmConfig := components.CreatePromptAgentAPIModelInputBackupLlmConfigDefault(components.BackupLLMDefault{/* values here */})
```

### BackupLLMDisabled

```go
promptAgentAPIModelInputBackupLlmConfig := components.CreatePromptAgentAPIModelInputBackupLlmConfigDisabled(components.BackupLLMDisabled{/* values here */})
```

### BackupLLMOverride

```go
promptAgentAPIModelInputBackupLlmConfig := components.CreatePromptAgentAPIModelInputBackupLlmConfigOverride(components.BackupLLMOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelInputBackupLlmConfig.Type {
	case components.PromptAgentAPIModelInputBackupLlmConfigTypeDefault:
		// promptAgentAPIModelInputBackupLlmConfig.BackupLLMDefault is populated
	case components.PromptAgentAPIModelInputBackupLlmConfigTypeDisabled:
		// promptAgentAPIModelInputBackupLlmConfig.BackupLLMDisabled is populated
	case components.PromptAgentAPIModelInputBackupLlmConfigTypeOverride:
		// promptAgentAPIModelInputBackupLlmConfig.BackupLLMOverride is populated
}
```
