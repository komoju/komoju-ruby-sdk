# Komoju::CreateCustomerRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **payment_details** | [**PaymentDetailsOnlyCreditCards**](PaymentDetailsOnlyCreditCards.md) |  | [optional] |
| **email** | **String** | Customer&#39;s email address. | [optional] |
| **metadata** | **Object** | Store any additional data you want to associate with the customer. The object&#39;s keys and values must be strings. Keys have a maximum length of 30 characters. Values have a maximum length of 2000 characters. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::CreateCustomerRequest.new(
  currency: null,
  payment_details: null,
  email: null,
  metadata: null
)
```

