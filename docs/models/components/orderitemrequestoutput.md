# OrderItemRequestOutput


## Supported Types

### DubOrderItemRequest

```go
orderItemRequestOutput := components.CreateOrderItemRequestOutputDub(components.DubOrderItemRequest{/* values here */})
```

### SubtitleOrderItemRequest

```go
orderItemRequestOutput := components.CreateOrderItemRequestOutputSubtitles(components.SubtitleOrderItemRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch orderItemRequestOutput.Type {
	case components.OrderItemRequestOutputTypeDub:
		// orderItemRequestOutput.DubOrderItemRequest is populated
	case components.OrderItemRequestOutputTypeSubtitles:
		// orderItemRequestOutput.SubtitleOrderItemRequest is populated
}
```
