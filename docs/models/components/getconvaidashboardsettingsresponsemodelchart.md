# GetConvAIDashboardSettingsResponseModelChart


## Supported Types

### DashboardCallSuccessChartModel

```go
getConvAIDashboardSettingsResponseModelChart := components.CreateGetConvAIDashboardSettingsResponseModelChartCallSuccess(components.DashboardCallSuccessChartModel{/* values here */})
```

### DashboardCriteriaChartModel

```go
getConvAIDashboardSettingsResponseModelChart := components.CreateGetConvAIDashboardSettingsResponseModelChartCriteria(components.DashboardCriteriaChartModel{/* values here */})
```

### DashboardDataCollectionChartModel

```go
getConvAIDashboardSettingsResponseModelChart := components.CreateGetConvAIDashboardSettingsResponseModelChartDataCollection(components.DashboardDataCollectionChartModel{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch getConvAIDashboardSettingsResponseModelChart.Type {
	case components.GetConvAIDashboardSettingsResponseModelChartTypeCallSuccess:
		// getConvAIDashboardSettingsResponseModelChart.DashboardCallSuccessChartModel is populated
	case components.GetConvAIDashboardSettingsResponseModelChartTypeCriteria:
		// getConvAIDashboardSettingsResponseModelChart.DashboardCriteriaChartModel is populated
	case components.GetConvAIDashboardSettingsResponseModelChartTypeDataCollection:
		// getConvAIDashboardSettingsResponseModelChart.DashboardDataCollectionChartModel is populated
	default:
		// Unknown type - use getConvAIDashboardSettingsResponseModelChart.GetUnknownRaw() for raw JSON
}
```
