# Komoju::UpdateCustomerRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **payment_details** | [**PaymentDetailsOnlyCreditCards**](PaymentDetailsOnlyCreditCards.md) |  | [optional] |
| **email** | **String** |  | [optional] |
| **metadata** | **Object** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::UpdateCustomerRequest.new(
  currency: null,
  payment_details: null,
  email: null,
  metadata: null
)
```

