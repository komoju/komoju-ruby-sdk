# Komoju::PaySessionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **redirect_url** | **String** | URL to redirect the customer to after submitting payment details, or null if no redirect is required. |  |
| **status** | [**SessionStatus**](SessionStatus.md) |  |  |
| **payment** | [**Payment**](Payment.md) |  | [optional] |
| **app_url** | **String** | URL for the payment app. Only present for offsite payments with a QR/app URL. | [optional] |
| **customer** | [**SubscriptionCustomer**](SubscriptionCustomer.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaySessionResponse.new(
  redirect_url: null,
  status: null,
  payment: null,
  app_url: null,
  customer: null
)
```

