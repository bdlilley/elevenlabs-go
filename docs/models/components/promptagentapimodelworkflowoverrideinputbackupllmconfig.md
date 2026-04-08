# PromptAgentAPIModelWorkflowOverrideInputBackupLlmConfig

Configuration for backup LLM cascading. Can be disabled, use system defaults, or specify custom order.


## Supported Types

### BackupLLMDefault

```go
promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig := components.CreatePromptAgentAPIModelWorkflowOverrideInputBackupLlmConfigBackupLLMDefault(components.BackupLLMDefault{/* values here */})
```

### BackupLLMDisabled

```go
promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig := components.CreatePromptAgentAPIModelWorkflowOverrideInputBackupLlmConfigBackupLLMDisabled(components.BackupLLMDisabled{/* values here */})
```

### BackupLLMOverride

```go
promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig := components.CreatePromptAgentAPIModelWorkflowOverrideInputBackupLlmConfigBackupLLMOverride(components.BackupLLMOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig.Type {
	case components.PromptAgentAPIModelWorkflowOverrideInputBackupLlmConfigTypeBackupLLMDefault:
		// promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig.BackupLLMDefault is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputBackupLlmConfigTypeBackupLLMDisabled:
		// promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig.BackupLLMDisabled is populated
	case components.PromptAgentAPIModelWorkflowOverrideInputBackupLlmConfigTypeBackupLLMOverride:
		// promptAgentAPIModelWorkflowOverrideInputBackupLlmConfig.BackupLLMOverride is populated
}
```
