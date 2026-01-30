# Komoju::UpdatePaymentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional] |
| **metadata** | **Object** |  | [optional] |
| **payment_details** | [**PaymentDetailsAll**](PaymentDetailsAll.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::UpdatePaymentRequest.new(
  description: null,
  metadata: null,
  payment_details: null
)
```

