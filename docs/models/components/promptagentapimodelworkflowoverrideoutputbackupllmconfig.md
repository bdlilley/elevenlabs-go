# PromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig

Configuration for backup LLM cascading. Can be disabled, use system defaults, or specify custom order.


## Supported Types

### BackupLLMDefault

```go
promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig := components.CreatePromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfigBackupLLMDefault(components.BackupLLMDefault{/* values here */})
```

### BackupLLMDisabled

```go
promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig := components.CreatePromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfigBackupLLMDisabled(components.BackupLLMDisabled{/* values here */})
```

### BackupLLMOverride

```go
promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig := components.CreatePromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfigBackupLLMOverride(components.BackupLLMOverride{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig.Type {
	case components.PromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfigTypeBackupLLMDefault:
		// promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig.BackupLLMDefault is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfigTypeBackupLLMDisabled:
		// promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig.BackupLLMDisabled is populated
	case components.PromptAgentAPIModelWorkflowOverrideOutputBackupLlmConfigTypeBackupLLMOverride:
		// promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig.BackupLLMOverride is populated
	default:
		// Unknown type - use promptAgentAPIModelWorkflowOverrideOutputBackupLlmConfig.GetUnknownRaw() for raw JSON
}
```
