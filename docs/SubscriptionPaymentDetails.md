# Komoju::SubscriptionPaymentDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type for this subscription. |  |
| **month** | **String** | Card expiry month. |  |
| **year** | **String** | Card expiry year. |  |
| **email** | **String** | Customer&#39;s email address. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SubscriptionPaymentDetails.new(
  type: null,
  month: null,
  year: null,
  email: null
)
```

