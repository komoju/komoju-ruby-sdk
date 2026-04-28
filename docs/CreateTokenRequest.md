# Komoju::CreateTokenRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **payment_details** | [**PaymentDetailsOnlyCreditCards**](PaymentDetailsOnlyCreditCards.md) |  |  |
| **platform_details** | [**ProcessingMerchant**](ProcessingMerchant.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CreateTokenRequest.new(
  currency: null,
  payment_details: null,
  platform_details: null
)
```

