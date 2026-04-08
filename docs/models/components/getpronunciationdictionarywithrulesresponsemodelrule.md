# GetPronunciationDictionaryWithRulesResponseModelRule


## Supported Types

### PronunciationDictionaryAliasRuleResponseModel

```go
getPronunciationDictionaryWithRulesResponseModelRule := components.CreateGetPronunciationDictionaryWithRulesResponseModelRuleAlias(components.PronunciationDictionaryAliasRuleResponseModel{/* values here */})
```

### PronunciationDictionaryPhonemeRuleResponseModel

```go
getPronunciationDictionaryWithRulesResponseModelRule := components.CreateGetPronunciationDictionaryWithRulesResponseModelRulePhoneme(components.PronunciationDictionaryPhonemeRuleResponseModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getPronunciationDictionaryWithRulesResponseModelRule.Type {
	case components.GetPronunciationDictionaryWithRulesResponseModelRuleTypeAlias:
		// getPronunciationDictionaryWithRulesResponseModelRule.PronunciationDictionaryAliasRuleResponseModel is populated
	case components.GetPronunciationDictionaryWithRulesResponseModelRuleTypePhoneme:
		// getPronunciationDictionaryWithRulesResponseModelRule.PronunciationDictionaryPhonemeRuleResponseModel is populated
}
```
