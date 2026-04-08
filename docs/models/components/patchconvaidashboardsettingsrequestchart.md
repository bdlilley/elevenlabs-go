# PatchConvAIDashboardSettingsRequestChart


## Supported Types

### DashboardCallSuccessChartModel

```go
patchConvAIDashboardSettingsRequestChart := components.CreatePatchConvAIDashboardSettingsRequestChartCallSuccess(components.DashboardCallSuccessChartModel{/* values here */})
```

### DashboardCriteriaChartModel

```go
patchConvAIDashboardSettingsRequestChart := components.CreatePatchConvAIDashboardSettingsRequestChartCriteria(components.DashboardCriteriaChartModel{/* values here */})
```

### DashboardDataCollectionChartModel

```go
patchConvAIDashboardSettingsRequestChart := components.CreatePatchConvAIDashboardSettingsRequestChartDataCollection(components.DashboardDataCollectionChartModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch patchConvAIDashboardSettingsRequestChart.Type {
	case components.PatchConvAIDashboardSettingsRequestChartTypeCallSuccess:
		// patchConvAIDashboardSettingsRequestChart.DashboardCallSuccessChartModel is populated
	case components.PatchConvAIDashboardSettingsRequestChartTypeCriteria:
		// patchConvAIDashboardSettingsRequestChart.DashboardCriteriaChartModel is populated
	case components.PatchConvAIDashboardSettingsRequestChartTypeDataCollection:
		// patchConvAIDashboardSettingsRequestChart.DashboardDataCollectionChartModel is populated
}
```
