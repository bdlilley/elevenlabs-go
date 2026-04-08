<!-- Start SDK Example Usage [usage] -->
```go
package main

import (
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"github.com/bdlilley/elevenlabs-go/models/components"
	"log"
)

func main() {
	ctx := context.Background()

	s := elevenlabsgo.New(
		elevenlabsgo.WithSecurity("YOUR_API_KEY"),
	)

	res, err := s.GetUserSubscriptionInfo(ctx)
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