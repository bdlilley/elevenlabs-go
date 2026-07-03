<!-- Start SDK Example Usage [usage] -->
```go
package main

import (
	"context"
	elevenlabsgo "github.com/bdlilley/elevenlabs-go"
	"log"
)

func main() {
	ctx := context.Background()

	s := elevenlabsgo.New(
		elevenlabsgo.WithSecurity("YOUR_API_KEY"),
	)

	res, err := s.GetUserInfo(ctx)
	if err != nil {
		log.Fatal(err)
	}
	if res.UserResponseModel != nil {
		// handle response
	}
}

```
<!-- End SDK Example Usage [usage] -->