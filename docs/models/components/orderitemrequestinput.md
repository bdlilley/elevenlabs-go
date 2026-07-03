# OrderItemRequestInput


## Supported Types

### DubOrderItemRequest

```go
orderItemRequestInput := components.CreateOrderItemRequestInputDub(components.DubOrderItemRequest{/* values here */})
```

### SubtitleOrderItemRequest

```go
orderItemRequestInput := components.CreateOrderItemRequestInputSubtitles(components.SubtitleOrderItemRequest{/* values here */})
```

## Union Discrimination

Use the `Type` field to determine which variant is active, then access the corresponding field:

```go
switch orderItemRequestInput.Type {
	case components.OrderItemRequestInputTypeDub:
		// orderItemRequestInput.DubOrderItemRequest is populated
	case components.OrderItemRequestInputTypeSubtitles:
		// orderItemRequestInput.SubtitleOrderItemRequest is populated
}
```
