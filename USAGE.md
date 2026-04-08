<!-- Start SDK Example Usage [usage] -->
```go
package main

import (
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"github.com/bdlilley/elevenlabs-go/optionalnullable"
	"log"
)

func main() {
	ctx := context.Background()

	s := elevenlabsgo.New(
		"https://api.example.com",
		elevenlabsgo.WithSecurity("YOUR_API_KEY"),
	)

	res, err := s.GetUserSubscriptionInfo(ctx, optionalnullable.From[string](nil))
	if err != nil {
		log.Fatal(err)
	}
	if res.ExtendedSubscriptionResponseModel != nil {
		switch res.ExtendedSubscriptionResponseModel.PendingChange.Type {
		case components.PendingChangeTypePendingSubscriptionSwitchResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingSubscriptionSwitchResponseModel is populated
		case components.PendingChangeTypePendingCancellationResponseModel:
			// res.ExtendedSubscriptionResponseModel.PendingChange.PendingCancellationResponseModel is populated
		}

	}
}

```
<!-- End SDK Example Usage [usage] -->