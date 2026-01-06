# Komoju::CreateTokenRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **payment_details** | [**PaymentDetailsOnlyCreditCards**](PaymentDetailsOnlyCreditCards.md) |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CreateTokenRequest.new(
  currency: null,
  payment_details: null
)
```

